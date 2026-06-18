# CES Sale Kit

> Bộ Skill Claude Code cho phòng Sale CES Global — gen proposal, báo giá, kịch bản tư vấn, email, xử lý objection, form khảo sát, hợp đồng chuẩn brand CES chỉ bằng vài câu prompt.

**Triết lý:** Sale gõ chân dung KH + nhu cầu → Skill ra output đúng brand, đúng portfolio, đúng tone. Sale chỉ tinh chỉnh + gửi.

---

## 🎯 7 Skill trong kit

| Skill | Dùng khi | Output |
|---|---|---|
| `ces-sale-proposal` | Gửi proposal cho KH B2B/B2C sau buổi tư vấn đầu | File MD/Word proposal chuẩn brand |
| `ces-sale-quote` | KH hỏi báo giá | Bảng báo giá có học phí + ưu đãi + thanh toán |
| `ces-sale-script` | Trước buổi gọi/gặp KH | Kịch bản tư vấn theo persona KH |
| `ces-sale-email` | Gửi email follow-up KH | Email template cold/warm/closing |
| `ces-sale-objection` | KH nêu khúc mắc | Script trả lời objection + evidence |
| `ces-sale-survey` | Khảo sát KH B2B sau workshop/buổi học | Form Google Form spec + câu hỏi |
| `ces-sale-contract` | Chốt deal, soạn hợp đồng | Hợp đồng nguyên tắc/dịch vụ mẫu |

---

## 🚀 Cài 5 phút

Xem `INSTALL.md` — clone repo, cài Claude Code, đăng ký skills.

---

## 📚 Knowledge nội bộ (Skill tự đọc khi gen)

- `knowledge/brand-ces-global.md` — Brand voice + tagline + màu + font
- `knowledge/portfolio-khoa-ces.md` — Toàn bộ khóa đang chạy + sắp ra + giá placeholder
- `knowledge/personas-khach-hang.md` — 5 chân dung KH B2B/B2C
- `knowledge/usp-vs-competitor.md` — Điểm mạnh CES so với đối thủ
- `knowledge/objection-bank.md` — 12 objection + câu trả lời mẫu

---

## 🤖 Agent Team — 1 prompt sinh đội 4 nhân viên ảo ⭐

**4 Agent** chạy song song hỗ trợ 1 Sale từ A-Z:

| Agent | Vai trò | Output |
|---|---|---|
| **Discovery** | Phân tích pain · match persona · 5 câu discovery | `01-discovery.md` |
| **Content** | Proposal · báo giá · email | `02-proposal.md` + `03-quote.md` + `04-email.md` |
| **Pitch** | Kịch bản · objection custom | `05-script.md` + `06-objections.md` |
| **Closing** | Follow-up timeline · HĐ · email closing | `07` + `08a-contract.md` + `08b-email.md` |

→ Sale gõ 1 prompt natural language → 8 file ready trong 5-10 phút.

→ Hướng dẫn: **[AGENTS.md](AGENTS.md)**

---

## 📅 Lịch sử

- **18/06/2026** — Tạo repo (TA + buổi training Sale 8h30 19/06)

---

*Maintained by Phòng Dự Án CES Global · Skill chuẩn theo `ces-fb` brand pattern.*
