# Slide bài giảng — Training Sale 90' · 19/06/2026

> 15 slide markdown. Export PDF hoặc dùng Marp/Slidev render. Mỗi slide 1 ý chính, không nhồi.

---

## Slide 1 — Cover

```
TRAINING SALE
─────────────
Claude + Claude Code + Skill chuẩn brand CES
+ MCP tích hợp

90 phút · 08h30-10h00 · 19/06/2026
Tuấn Anh — Lead Phòng Dự Án CES Global

> "Đồng hành chuyển đổi AI cùng doanh nghiệp"
```

---

## Slide 2 — Tại sao buổi này

```
SẾP TIỆP GIAO 18/06:
"Sắp xếp training sale về các khóa đang chạy"

NHƯNG MÌNH KHÔNG NÓI VỀ KHÓA HÔM NAY.

VÌ:
- Đại đang tư vấn 1 person company khó
- KH dùng Claude rồi, hỏi: "Sao phải học CES?"
- Sale cần CÔNG CỤ, không cần thêm slide khóa

→ Hôm nay: Sale học DÙNG AI tự sinh
  proposal · báo giá · kịch bản · email
  trong 5 phút thay vì 1 tiếng.
```

---

## Slide 3 — Output cuối buổi

```
SAU 90 PHÚT, MỖI SALE CÓ:

✅ Claude Code + 7 Skill `ces-sale-*` cài sẵn
✅ Tự gen proposal/báo giá/script trong 5'
✅ 3 MCP truy cập vault CES + SOP + automation
✅ Đại có proposal mẫu cho case hôm qua

REPO: github.com/andyluu98/ces-sale-kit
```

---

## Slide 4 — Chương trình 6 phần

```
1. Mở đầu                    5'  (08h30-08h35)
2. Claude basic cho Sale     15' (08h35-08h50)
3. Claude Code + Cowork      20' (08h50-09h10)
4. ⭐ Cowork tạo Skill        25' (09h10-09h35)
5. MCP tích hợp              15' (09h35-09h50)
6. Case Đại + Q&A            10' (09h50-10h00)
                            ─────
                            90'
```

---

## Slide 5 — Demo nhanh (Phần 1)

```
GÕ TRONG CLAUDE CODE:

  /ces-sale-kich-ban

CLAUDE HỎI:
  - KH là ai? Persona nào? Mục tiêu?

TA NHẬP:
  - 1 person company, freelancer mkt
  - Persona 5, đã dùng Claude
  - Chốt: đặt demo

CLAUDE TRẢ:
  → Kịch bản 5 phần đầy đủ
  → 30 giây từ input đến output

→ ĐÂY LÀ CÁI CHÚNG TA SẼ HỌC BUILD.
```

---

## Slide 6 — Claude basic (Phần 2)

```
4 KHÁI NIỆM SALE PHẢI BIẾT:

1. Claude.ai — web, ai cũng dùng
2. Project — gom context 1 KH/dự án
3. Style — giữ tone CES Global
4. Prompt template — 5 mẫu cơ bản

→ Sale có Pro 20$/tháng là đủ.
```

---

## Slide 7 — 5 Prompt Sale dùng hàng ngày

```
1. SOẠN PROPOSAL:
   "Soạn proposal khóa {X} cho {KH},
    persona {P}, pain {Y}, brand CES."

2. SOẠN BÁO GIÁ:
   "Báo giá khóa {X}, {N} HV, ưu đãi {Z}%,
    thanh toán 2 đợt."

3. SOẠN KỊCH BẢN:
   "Kịch bản tư vấn {KH}, persona {P},
    mục tiêu {chốt/demo}, 30'."

4. XỬ LÝ OBJECTION:
   "KH nói '{nguyên văn}'. Trả lời theo
    tone CES?"

5. SOẠN EMAIL:
   "Email follow-up sau proposal, 3 ngày
    chưa rep, tone nhẹ."
```

---

## Slide 8 — Claude Code là gì (Phần 3)

```
CLAUDE CODE = CLAUDE Ở TERMINAL

KHÁC CLAUDE.AI:
  ✅ Đọc cả folder trên máy
  ✅ Viết Skill custom
  ✅ Dùng MCP (truy cập vault, CRM, desktop)

CÀI 5 PHÚT:
  Windows:
    iwr -useb https://claude.ai/install.ps1 | iex
  Mac:
    curl -fsSL https://claude.ai/install.sh | sh

  → Mở terminal → `claude` → login
```

---

## Slide 9 — Cowork mode

```
2 NGƯỜI CÙNG 1 SESSION

DEMO LIVE:
- TA mở Claude Code
- Đại cùng vào
- 2 người cùng build Skill cho case của Đại
- Cùng debug, cùng test

→ KHÁC làm 1 mình:
  Sale 1 gặp objection mới → cả team
  thấy + bổ sung vào skill ngay
```

---

## Slide 10 — Skill là gì

```
SKILL ≠ PROMPT THƯỜNG

  PROMPT: gõ mỗi lần, không tái dùng

  SKILL: folder có SKILL.md + knowledge files
         → workflow chuẩn hóa
         → share team
         → versioning trên Git

PATTERN CES ĐÃ DÙNG:
  - ces-fb       (Marketing — viết caption FB)
  - ces-training (Đào tạo — soạn curriculum)
  - ces-sale-kit (Sale — GIỜ MÌNH BUILD CHO TEAM)
```

---

## Slide 11 — Cowork tạo Skill LIVE (Phần 4) ⭐

```
CLONE REPO:

  git clone https://github.com/andyluu98/ces-sale-kit.git
  cd ces-sale-kit

CẤU TRÚC:
  ces-sale-kit/
  ├── .claude/skills/
  │   ├── ces-sale-de-xuat/    ← Gen đề xuất
  │   ├── ces-sale-bao-gia/       ← Gen báo giá
  │   ├── ces-sale-kich-ban/      ← Kịch bản tư vấn
  │   ├── ces-sale-email/       ← 8 email mẫu
  │   ├── ces-sale-xu-ly-tu-choi/   ← Xử lý khúc mắc
  │   ├── ces-sale-khao-sat/      ← Form khảo sát
  │   └── ces-sale-hop-dong/    ← Hợp đồng
  ├── knowledge/                ← Brand + Portfolio + Persona
  └── templates/                ← Khung output
```

---

## Slide 12 — Demo 3 Skill LIVE (12 phút)

```
DEMO 1 — ces-sale-kich-ban (4')
  "Kịch bản gọi cold persona 5,
   KH đã dùng Claude"
  → Output 5 phần

DEMO 2 — ces-sale-xu-ly-tu-choi (4')
  "KH nói: Bên nào cũng chạy Claude"
  → Script trả lời + evidence

DEMO 3 — ces-sale-de-xuat (4')
  Input case Đại
  → Proposal 8 phần hoàn chỉnh
  → Placeholder {HOC_PHI} {UU_DAI} fill sau
```

---

## Slide 13 — Agent Team: 4 nhân viên ảo (Phần 5) ⭐

```
SKILL vs AGENT TEAM:

Skill rời:  gõ 1 lệnh → 1 file
Agent Team: gõ 1 prompt → 8 file

ĐỘI 4 AGENT cho 1 Sale:

  🤖 Discovery   → Pain · Persona · Câu hỏi
  🤖 Content     → Proposal · Báo giá · Email
  🤖 Pitch       → Kịch bản · Objection
  🤖 Closing     → Timeline · HĐ · Email chốt

CÁCH GỌI: 1 prompt natural language

  "Case mới: KH = ... Tạo Agent Team
   xử lý, em cần tài liệu trước 9h mai."

→ 4 Agent chạy SONG SONG ~8 phút
→ Output: outputs/{kh-slug}/01-08*.md

→ Chi tiết: AGENTS.md ở root repo
```

---

## Slide 14 — Case Đại Q&A (Phần 6)

```
ROLE-PLAY:

  KH = freelancer marketing, 1 mình
  Pain = dùng Claude 6 tháng rồi
         nhưng không scale được
  Hỏi = "Sao phải học CES?"
  Ngân sách = <20tr

ĐẠI THỬ:
  /ces-sale-xu-ly-tu-choi → "Bên nào cũng dùng Claude"
  /ces-sale-kich-ban → Kịch bản gọi
  /ces-sale-de-xuat → Đề xuất khóa OPC + USP

→ 3 PHÚT CÓ ĐỦ 3 OUTPUT GỬI KH.
```

---

## Slide 15 — Sau buổi này

```
TUẦN NÀY (22-28/06):
  Sale dùng Skill thực tế · feedback bug

TUẦN SAU (29/06-05/07):
  TA + Hải patch · add KH thực vào knowledge

THÁNG 7:
  Đo: Sale tiết kiệm bao nhiêu giờ/tuần?
       Tỷ lệ chốt deal thay đổi?

REPO: github.com/andyluu98/ces-sale-kit
HỖ TRỢ KỸ THUẬT: Hải (Tech Lead) · TA

> "Kinh doanh hiệu quả — Phát triển bền vững."

Cảm ơn cả team!
```

---

## Render slide

### Cách 1 — Marp (khuyến nghị)

```bash
npm install -g @marp-team/marp-cli
marp slide-bai-giang.md -o slide.pdf
```

### Cách 2 — Slidev

```bash
npm i -g @slidev/cli
slidev slide-bai-giang.md
```

### Cách 3 — PowerPoint manual

Copy từng slide block trên vào PowerPoint, áp theme:
- Màu nền: Navy `#0B2349`
- Chữ: White / Teal `#00A99D`
- Accent: Gold `#F5A623`
- Font: Be Vietnam Pro Bold
