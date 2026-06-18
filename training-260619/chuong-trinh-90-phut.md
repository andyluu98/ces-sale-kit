# Chương trình Training Sale — 90 phút · 08h30-10h00 · 19/06/2026

> **Hướng:** Dạy Sale CÁCH DÙNG Claude + Claude Code + cowork tạo Skill chuẩn brand CES + MCP. KHÔNG phải chỉ giới thiệu portfolio.
>
> **Người dạy:** Tuấn Anh (Lead Phòng Dự Án)
> **Đối tượng:** Team Sale CES Global (A. Linh + Đại + ...)
> **Bối cảnh:** Sếp Tiệp giao 18/06 — Đại đang tư vấn case 1 person company khó, Sale chưa biết show điểm mạnh CES.

## Mục tiêu buổi

Cuối buổi, mỗi Sale có:
- ✅ Claude Code + 7 Skill `ces-sale-*` cài sẵn trên máy
- ✅ Hiểu cowork mode + tự gen proposal/kịch bản/báo giá/email/objection trong 5 phút
- ✅ Biết 3 MCP để truy cập vault CES + SOP + automation desktop
- ✅ Đại có proposal mẫu cho case 1 person company

## Chương trình 6 phần

| # | Phần | Phút | Khung giờ | Nội dung chính |
|---|---|---|---|---|
| 1 | **Mở đầu + mục tiêu** | 5' | 08h30–08h35 | Bối cảnh case Đại · Vì sao Sale cần Claude · Demo nhanh output buổi |
| 2 | **Claude basic cho Sale** | 15' | 08h35–08h50 | Claude.ai · Project · Style · 5 prompt template cơ bản |
| 3 | **Claude Code + Cowork mode** | 20' | 08h50–09h10 | Cài Claude Code · Cowork session · Skill là gì · pattern repo |
| 4 | ⭐ **Cowork tạo Skill `ces-sale-kit`** | 25' | 09h10–09h35 | Demo LIVE: clone repo · chạy thử 3 skill (proposal · script · email) |
| 5 | **Agent Team — 1 prompt sinh ekip 4 Agent** ⭐ | 15' | 09h35–09h50 | 4 Agent: Discovery · Content · Pitch · Closing — demo case Đại |
| 6 | **Case Đại + Q&A** | 10' | 09h50–10h00 | Role-play: dùng Skill cho case 1 person company · Q&A · Giao kit cho team |

---

## Phần 1 — Mở đầu (5')

**Mở:**
> "Sáng nay 90' mình không nói về portfolio khóa — Sếp Tiệp giao em đào tạo các anh chị CÁCH DÙNG AI để tự sinh proposal/báo giá/kịch bản trong 5 phút thay vì 1 tiếng. Khi xong buổi này, các anh chị về máy gõ `/ces-sale-proposal` cái là ra proposal hoàn chỉnh."

**Demo nhanh (90 giây):**
- Mở Claude Code
- Gõ: `/ces-sale-script` → KH B2C, 1 person company, biết Claude rồi
- Skill ra kịch bản tư vấn 5 phần đầy đủ trên màn hình
- "Đây là output 30 giây — buổi nay học cách build cái này."

**Câu hỏi mở:** "Anh chị hiện tốn bao nhiêu giờ/tuần soạn proposal/báo giá thủ công?"

---

## Phần 2 — Claude basic cho Sale (15')

**2.1 Claude.ai là gì** (3')
- Khác ChatGPT: context window dài, follow instruction tốt hơn
- 3 plan: Free / Pro 20$ / Max 100$ → Sale dùng Pro là đủ

**2.2 Project — gom context KH** (4')
- Demo tạo Project "KH X — Tập đoàn Y"
- Upload: proposal cũ + brief khóa CES + persona
- Mỗi message trong Project sẽ có context KH X
- → Sale không phải paste lại context mỗi lần

**2.3 Style — giữ tone CES** (3')
- Tạo Style: "Tone CES Global — chuyên nghiệp · tiên phong · thực chiến · nhân văn. Xưng anh/chị + em. Không quý khách. Có số liệu, không chung chung."
- Mọi message dùng Style này → output đúng brand

**2.4 5 Prompt template cơ bản** (5')

| # | Use case | Prompt |
|---|---|---|
| 1 | Gen proposal | "Soạn proposal khóa {X} cho {KH} — persona {P}, pain {Y}. Format theo brand CES." |
| 2 | Gen báo giá | "Soạn báo giá khóa {X}, {N} HV, ưu đãi {Z}%, thanh toán {2 đợt}." |
| 3 | Gen kịch bản | "Kịch bản tư vấn KH {tên}, persona {P}, mục tiêu {chốt deal/đặt demo}, 30 phút." |
| 4 | Xử lý objection | "KH nói '{nguyên văn}'. Em trả lời thế nào theo tone CES?" |
| 5 | Gen email | "Email follow-up sau proposal cho {KH}, 3 ngày chưa rep, tone nhẹ không push." |

→ **Thực hành 2 phút:** mỗi Sale thử gen 1 cái → so kết quả.

---

## Phần 3 — Claude Code + Cowork (20')

**3.1 Claude Code là gì** (3')
- Phiên bản terminal — chạy local, đọc file trên máy, gen code/file
- Hơn Claude.ai ở: đọc cả folder, viết Skill custom, dùng MCP

**3.2 Cài 5 phút** (5')
- Windows: `iwr -useb https://claude.ai/install.ps1 | iex` (PowerShell)
- Mac: `curl -fsSL https://claude.ai/install.sh | sh`
- Mở terminal → gõ `claude` → login

**3.3 Cowork mode** (5')
- 2 người cùng dùng 1 session Claude → cùng debug, cùng build Skill
- Demo: TA + Đại cùng vào, cùng gen proposal cho case Đại

**3.4 Skill là gì** (7')
- Skill = folder có `SKILL.md` định nghĩa workflow + knowledge files
- Khác prompt thường: có hệ thống, tái dùng, share team
- Pattern: `ces-fb` đã dùng cho Marketing — giờ làm `ces-sale-kit` cho Sale

---

## Phần 4 — Cowork tạo Skill `ces-sale-kit` LIVE (25') ⭐

**Đây là phần CORE — Sale ra về có Skill cài sẵn.**

**4.1 Clone repo** (3')
```bash
cd ~
git clone https://github.com/andyluu98/ces-sale-kit.git
cd ces-sale-kit
```

**4.2 Tour repo** (5')
- `.claude/skills/` — 7 skill `ces-sale-*`
- `knowledge/` — brand + portfolio + persona + USP + objection bank
- `templates/` — proposal · báo giá · email · hợp đồng
- `training-260619/` — file buổi nay

**4.3 Demo 3 skill chính** (12')

**Demo 1 — `ces-sale-script` (4')**
- TA mở Claude Code trong repo
- Gõ: "Soạn kịch bản gọi cold cho persona 5 (1 person company), KH đã thử Claude rồi"
- Skill tự đọc `personas-khach-hang.md` + `objection-bank.md`
- Output kịch bản 5 phần (mở · discovery · pitch · objection · closing)
- TA copy-paste ra → Đại đọc thử

**Demo 2 — `ces-sale-objection` (4')**
- Đại nói: "KH em hôm qua nói 'Bên nào cũng chạy Claude'"
- Gõ: "Objection: 'Bên nào cũng chạy Claude'. Persona 5. Tone lịch sự nhẹ."
- Output script trả lời + evidence + bước tiếp theo

**Demo 3 — `ces-sale-proposal` (4')**
- Đại nhập input: KH = "Founder startup 8 người, ngành EdTech, pain dạy AI cho team"
- Gõ: `/ces-sale-proposal`
- Skill hỏi 6 câu → Đại trả lời nhanh
- Output proposal 8 phần với placeholder `{HOC_PHI}` `{UU_DAI}`

**4.4 Cowork: cả team build chung 1 Skill cải tiến** (5')
- Tất cả Sale cùng vào edit `knowledge/portfolio-khoa-ces.md`
- Thêm vào 2 khóa mới (mỗi Sale thêm 1 mục)
- Test lại Skill — output có khóa mới ngay

---

## Phần 5 — Agent Team: 1 prompt sinh ekip 4 Agent (15') ⭐

**Concept** (3')
- Skill = đồ nghề rời (gõ 1 lệnh ra 1 file)
- Agent Team = ekip 4 nhân viên ảo (gõ 1 prompt → 4 Agent chạy song song → 8 file ready)
- 4 vai trò: **Discovery** · **Content** · **Pitch** · **Closing**

**Bảng 4 Agent** (3')

| Agent | Vai trò | Output |
|---|---|---|
| 1. Discovery | Pain · persona · 5 câu hỏi | `01-discovery.md` |
| 2. Content | Proposal · báo giá · email | `02-04 .md` |
| 3. Pitch | Kịch bản · objection custom | `05-06 .md` |
| 4. Closing | Timeline · HĐ · email chốt | `07-08 .md` |

**Demo LIVE case Đại** (9')

TA gõ trong Claude Code:
```
Case mới: KH = Nguyễn Văn A, founder startup EdTech 8 người,
đã dùng Claude.ai 6 tháng, hỏi "sao phải học CES".
Ngân sách <20tr. Sáng mai 10h gọi follow-up.

Tạo Agent Team xử lý case này, em cần đủ tài liệu trước 9h sáng mai.
```

Claude Code:
- 4 Agent spawn song song
- ~8 phút chạy xong 8 file
- Sale review → fill placeholder → gửi KH

→ Chi tiết: file `AGENTS.md` ở root repo.

---

## Phần 6 — Case Đại + Q&A (10')

**6.1 Role-play case Đại** (5')

Đại nhập:
- KH: 1 person company, freelancer marketing
- Đã dùng Claude.ai 6 tháng
- Hỏi: "Sao tôi phải học CES khi Claude tôi tự xài được?"
- Ngân sách: <20tr

→ Đại gõ `/ces-sale-objection` + `/ces-sale-script` + `/ces-sale-proposal`
→ 3 phút có: kịch bản tư vấn + script trả lời objection + proposal phù hợp

**Output kỳ vọng:** Đại có file proposal + script in/share luôn cho KH.

**6.2 Q&A** (4')

Câu hỏi dự kiến:
- "Em không biết code, có dùng được không?" → Có, Skill che hết phần code
- "Skill có thay GV không?" → Không, Skill là công cụ, GV vẫn cần
- "Output gen ra có gửi thẳng KH được không?" → Cần review + fill placeholder

**6.3 Giao kit + bước tiếp theo** (1')

- Repo: `github.com/andyluu98/ces-sale-kit` (clone là dùng được)
- Hỗ trợ kỹ thuật: Hải · TA
- Feedback Skill nào còn yếu → PR vào repo, team dùng chung

---

## Tài liệu phát Sale ra về

1. 📄 Cheat sheet 1 trang (chuong-trinh-90-phut.md này, có thể in tóm tắt)
2. 💻 Repo `ces-sale-kit` (link GitHub)
3. 🔌 Hướng dẫn cài 3 MCP (`mcp-cho-sale.md`)
4. 📋 Prompt cheatsheet 20 prompt mẫu (`prompt-cheatsheet.md`)

---

## Sau buổi — Bước tiếp theo

- **Tuần 4 (22-28/06):** Sale dùng Skill thực tế, feedback bug/missing
- **Tuần 5 (29/06-05/07):** TA + Hải patch Skill, add KH thực vào knowledge
- **Tháng 7:** Đo số liệu — Sale tiết kiệm bao nhiêu giờ/tuần, tỷ lệ chốt thay đổi không
