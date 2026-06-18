# Agent Team — Đội hỗ trợ 1 Sale

> 1 prompt natural language → 4 Agent chạy song song → đủ tài liệu gửi KH trong 5-10 phút.

## Tổng quan

| Agent | Vai trò | Output | Time |
|---|---|---|---|
| **1. Discovery** | Phân tích pain · match persona · 5 câu discovery | `01-discovery.md` | ~2' |
| **2. Content** | Proposal · báo giá · email cover | `02-proposal.md` + `03-quote.md` + `04-email.md` | ~3' |
| **3. Pitch** | Kịch bản gọi/gặp · 5-7 objection custom · cheat sheet | `05-script.md` + `06-objections.md` | ~3' |
| **4. Closing** | Timeline follow-up · HĐ draft · email closing | `07-followup-timeline.md` + `08a-contract-draft.md` + `08b-email-closing.md` | ~2' |

→ 4 Agent chạy SONG SONG (parallel). Tổng ~5-10 phút có 8 file ready.

## Cách spawn Agent Team

**Sale gõ 1 prompt natural language trong Claude Code (đứng ở folder `ces-sale-kit`):**

### Mẫu prompt 1 — Case mới hoàn toàn

```
Case mới: KH = {tên}, {chức vụ}, {DN/cá nhân},
{ngành/lĩnh vực}, quy mô {N người},
đã dùng AI: {ChatGPT/Claude/chưa},
pain chính: {1-3 ý},
ngân sách: {khoảng tiền},
mục tiêu Sale: {gặp/chốt deal/đặt demo}.

Tạo Agent Team xử lý case này. Em cần đủ tài liệu trước {khi nào}.
```

### Mẫu prompt 2 — KH đã có proposal, đang follow-up

```
Case follow-up: KH = {tên},
đã gửi proposal {ngày}, chưa rep.
Persona đã match: P{X}.
Giai đoạn: B (đã nhận proposal, chưa OK giá).

Tạo Agent Team rà lại + chuẩn bị follow-up tuần này.
```

### Mẫu prompt 3 — KH đã OK giá, chuẩn bị chốt

```
Case closing: KH = {tên},
đã OK proposal + giá {Y}tr.
Chuẩn bị ký HĐ sáng mai 9h.

Tạo Agent Team gen HĐ + email closing + timeline thanh toán.
```

## Cách 4 Agent phối hợp

Khi Sale gõ prompt, **Claude Code chạy như sau:**

```
1. Lead (Claude main) đọc prompt → parse info KH
2. Dispatch SONG SONG:
   ├── Spawn Discovery Agent  ─┐
   ├── Spawn Content Agent     ├─ Cả 4 chạy đồng thời
   ├── Spawn Pitch Agent       │  (parallel agents)
   └── Spawn Closing Agent    ─┘
3. Mỗi Agent đọc knowledge files cần thiết
4. Mỗi Agent ghi output vào outputs/{kh-slug}/{N}-{name}.md
5. Lead gom kết quả, report tóm tắt cho Sale
6. Sale review → fill placeholder → gửi KH
```

**Phụ thuộc:**
- Content Agent + Pitch Agent + Closing Agent đều **đọc output Discovery** (file `01-discovery.md`) → cần Discovery xong trước 30 giây để 3 Agent kia có persona/pain để dùng
- Hoặc: Discovery chạy đầu (10-15 giây) → 3 Agent kia mới spawn (Claude tự handle dependency)

## Cấu trúc output

```
outputs/
└── {kh-slug}/                       ← 1 folder/KH (slug từ tên KH)
    ├── 01-discovery.md              ← Discovery Agent
    ├── 02-proposal.md               ← Content Agent
    ├── 03-quote.md                  ← Content Agent
    ├── 04-email.md                  ← Content Agent
    ├── 05-script.md                 ← Pitch Agent
    ├── 06-objections.md             ← Pitch Agent
    ├── 07-followup-timeline.md      ← Closing Agent
    ├── 08a-contract-draft.md        ← Closing Agent
    └── 08b-email-closing.md         ← Closing Agent
```

## Khi nào dùng Skill rời vs Agent Team

| Tình huống | Dùng gì |
|---|---|
| Chỉ cần 1 file (vd: gen 1 email follow-up) | **Skill rời** (`/ces-sale-email`) |
| Cần điều chỉnh 1 file đã có (vd: chỉnh proposal) | **Skill rời** (`/ces-sale-de-xuat`) |
| Sale gặp objection mới giữa buổi gọi → cần script gấp | **Skill rời** (`/ces-sale-xu-ly-tu-choi`) |
| KH MỚI hoàn toàn — cần đủ tài liệu pitch lần đầu | **Agent Team** (1 prompt) |
| KH đã pitch xong → chuẩn bị follow-up + chốt | **Agent Team** (1 prompt giai đoạn B/C) |
| KH có hồ sơ năng lực file PDF dài → cần đọc + phân tích | **Agent Team** (Discovery đọc PDF tự) |

→ Skill rời cho task lẻ. Agent Team cho case end-to-end.

## Ví dụ case Đại (1 person company)

**Sale gõ:**
```
Case mới: KH = Nguyễn Văn A, founder startup EdTech 8 người,
đã dùng Claude.ai 6 tháng, hỏi "sao phải học CES".
Ngân sách <20tr. Sáng mai 10h gọi follow-up.

Tạo Agent Team xử lý case này, em cần đủ tài liệu trước 9h sáng mai.
```

**Claude Code output (~8 phút):**
```
🤖 Discovery Agent đang chạy...
   ✅ Persona: P1 Founder Startup (alt: P5 nếu thiên về cá nhân)
   ✅ 7 pain analysis (top: team không buy-in · ROI chưa rõ)
   ✅ 5 câu discovery
   📁 outputs/nguyen-van-a/01-discovery.md

🤖 Content Agent đang chạy...
   ✅ Khóa đề xuất: AI Agent DN 6 buổi (fit P1)
   ✅ Proposal 8 phần (placeholder HOC_PHI)
   ✅ Báo giá <20tr ⚠️ nằm dưới range khóa public — đề xuất giảm còn 4 buổi hoặc thay khóa OPC
   ✅ Email cover Type 4
   📁 outputs/nguyen-van-a/02-04*.md

🤖 Pitch Agent đang chạy...
   ✅ Kịch bản gọi 30' (warm follow-up, không cold)
   ✅ 7 objection custom (top 1: "Đã dùng Claude rồi" — script + evidence repo ces-marketing-agent-kit)
   ✅ Cheat sheet 1 trang
   📁 outputs/nguyen-van-a/05-06*.md

🤖 Closing Agent đang chạy...
   ✅ Timeline giai đoạn A (mới gặp): T+1 email · T+3 follow-up · T+7 call
   ✅ HĐ draft (cảnh báo gửi pháp chế)
   ✅ Email closing (chưa dùng, để sẵn cho khi KH OK)
   📁 outputs/nguyen-van-a/07-08*.md

⏱️ Hoàn thành 8 file trong 8 phút.
📂 Mở folder: outputs/nguyen-van-a/

⚠️ Lưu ý Sale:
- Fill {HOC_PHI} sau khi xác nhận khóa cuối (AI Agent DN hay OPC)
- Verify ngân sách <20tr — có thể đề xuất 2 phương án (OPC + Workshop riêng)
- HĐ draft cần gửi pháp chế trước khi ký
```

→ Sale ngồi xem 8 phút → review 8 file → fill placeholder → gửi KH lúc 10h sáng.

## Khi Agent fail / output không ưng

1. **Spawn lại 1 Agent cụ thể** (không cần spawn cả 4):
   > "Pitch Agent gen kịch bản chưa phù hợp persona — spawn lại với context: KH thiên về kỹ thuật, không phải Founder thuần."

2. **Edit knowledge files** (vd: thêm objection mới vào `objection-bank.md`) → spawn lại Agent → ra đúng hơn

3. **Báo TA + Hải** để patch SKILL nếu pattern fail nhiều lần

## Mở rộng Agent Team (tương lai)

Có thể thêm các Agent mới:
- **Research Agent** — search web về DN KH (Google · LinkedIn · báo chí)
- **Translator Agent** — dịch proposal sang EN/CN cho KH nước ngoài
- **Analytics Agent** — sau khóa, phân tích feedback HV thành insight
- **Survey Agent** — gen + analyze form khảo sát

→ Khi thêm, mỗi Agent có file `.claude/agents/<name>.md` riêng. Pattern: kebab-case + 1 vai trò rõ.

---

*Đội Agent Team này là phiên bản nâng cấp Skill rời. Sale giỏi → dùng Agent Team. Sale mới → dùng Skill rời từng cái.*
