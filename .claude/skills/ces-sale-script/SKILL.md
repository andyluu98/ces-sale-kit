---
name: ces-sale-script
description: Gen kịch bản tư vấn Sale gặp/gọi KH theo persona. Dùng khi user nói "soạn kịch bản gọi", "kịch bản tư vấn KH [tên]", "script gặp KH [persona]", "/ces-sale-script". Output là script đọc lên dùng được — có lời thoại + objection + closing.
---

# CES Sale Script — Kịch bản tư vấn theo persona

Skill gen kịch bản Sale dùng cho cuộc gọi/buổi gặp đầu. KHÔNG phải lý thuyết sales — là kịch bản đọc lên DÙNG ĐƯỢC NGAY.

## Khi nào dùng

- Sale chuẩn bị gọi cold/warm KH lần đầu
- Sale chuẩn bị gặp KH trực tiếp (cafe / văn phòng KH)
- Sale gọi follow-up sau khi gửi proposal

## Bước 1 — Hỏi đầu vào

```
1. KH là ai? Tên + lĩnh vực + chức danh
2. Persona nào? (1-5 theo personas-khach-hang.md)
3. Loại buổi? (a) Cold call lần đầu · (b) Warm call sau form đăng ký · (c) Gặp face-to-face · (d) Follow-up sau proposal
4. Mục tiêu buổi này? (a) Đặt lịch demo · (b) Pitch khóa · (c) Chốt deal · (d) Lấy info
5. Thời lượng dự kiến? (a) 10' (gọi) · (b) 30' (zoom) · (c) 60' (face-to-face)
6. KH đã biết gì về CES rồi? (a) Lần đầu nghe · (b) Đã xem fanpage/web · (c) Đã đăng ký workshop · (d) Đã được giới thiệu từ HV cũ
```

## Bước 2 — Tự đọc knowledge

- `knowledge/personas-khach-hang.md` — ngôn ngữ + hook persona
- `knowledge/objection-bank.md` — objection có thể gặp
- `knowledge/portfolio-khoa-ces.md` — khóa nào fit persona

## Bước 3 — Output kịch bản (5 phần)

```markdown
# KỊCH BẢN TƯ VẤN — {Tên KH}
## Persona {N}: {Tên persona} · Mục tiêu: {Đặt demo / Pitch / Chốt}

> Thời lượng: {X}' · Tỷ lệ nói: KH 70% / Sale 30%

## Phần 1 — Mở đầu (1-2')

**Hook (chọn 1):**
- [Cold] "Em chào anh/chị [tên]. Em là [Sale name] từ CES Global. Em thấy [DN/profile KH] đang [pain quan sát được]. Em gọi 2-3 phút thôi, anh/chị có tiện không?"
- [Warm] "Em chào anh/chị [tên]. Hôm trước anh/chị đăng ký workshop AI Văn Phòng phải không ạ? Em gọi follow-up..."

**Mục tiêu phần này:** lấy 2-3 phút lắng nghe, KHÔNG pitch.

## Phần 2 — Discovery (5-15')

**4 nhóm câu hỏi (chọn 5-7 câu theo persona):**

### A. Warm-up
- "Anh/chị làm vai trò [chức danh] bao lâu rồi ạ?"
- "Công ty hiện có khoảng bao nhiêu nhân sự?"

### B. Quy trình hiện tại
- "Một tuần điển hình anh/chị tốn bao nhiêu giờ cho [pain quan sát]?"
- "Hiện team đang dùng tool gì để xử lý?"

### C. Pain & ưu tiên
- "Nếu giải quyết được [pain], anh/chị sẽ làm gì với thời gian dôi ra?"
- "3 ưu tiên lớn nhất quý này của anh/chị là gì?"

### D. Decision
- "Quyết định đầu tư đào tạo team thường ai duyệt?"
- "Anh/chị đang xem các giải pháp khác không?"

**Quy tắc:** lắng nghe 70%, hỏi tiếp khi KH chỉ trả lời 1 câu ngắn.

## Phần 3 — Pitch CES (5-10')

**Cấu trúc:**
1. **Tóm tắt lại pain KH vừa nói** (1-2 câu)
2. **Đề xuất khóa CES phù hợp** ({Tên khóa} từ portfolio match persona)
3. **3 USP key** (lấy từ usp-vs-competitor.md)
4. **Social proof cụ thể** (case study DN tương tự persona)

**Câu mẫu:**
> "Em hiểu — vấn đề anh/chị là [pain]. Ở CES, khóa [X] vừa làm cho [DN tương tự] — 3 tháng sau họ [outcome đo được]. Anh/chị muốn em gửi case study chi tiết không?"

## Phần 4 — Objection handling (5')

**Top 3 objection persona này hay gặp:**
{Lấy từ objection-bank.md → 3 cái phù hợp persona}

**Mỗi objection có sẵn script trả lời.**

**Quy tắc:** KHÔNG đối đầu — lặp lại + xác nhận + giải đáp.

## Phần 5 — Closing (2-3')

**3 lựa chọn closing (chọn theo signal KH):**

- **Closing mạnh (KH rõ ràng quan tâm):**
  > "Em đề xuất 2 bước: (1) Em gửi proposal chi tiết trong 24h, (2) Mình họp lại trong tuần sau để chốt. Anh/chị nhận proposal qua email hay Zalo tiện hơn?"

- **Closing trung bình (KH còn cân nhắc):**
  > "Em gửi anh/chị 3 thứ để tham khảo: proposal + case study + link cộng đồng HV. Em call lại sau 3 ngày — không push, chỉ check thông tin còn thiếu gì."

- **Closing nhẹ (KH chưa sẵn sàng):**
  > "Em hiểu giờ chưa phải lúc. Em note 1 reminder Q3 để gọi lại. Trong lúc đó em gửi anh/chị 1 ebook free về xu hướng AI ngành [ngành KH] để tham khảo nhé."

**Đừng push 3 lần** — nếu KH từ chối 2 lần, dừng và để reminder.

## Cheat sheet 1 trang (in ra cầm theo)

```
HOOK: [1 câu mở đầu theo type]
DISCOVERY (chọn 5/7 câu): ...
PITCH: [Tóm pain] → [Khóa X] → [3 USP] → [Case Y]
OBJECTION (top 3 persona): ...
CLOSING: [Mạnh / TB / Nhẹ]
```
```

## Bước 4 — Trả thêm

Sau khi gen kịch bản, hỏi user:
> "Anh/chị muốn em gen luôn 3 case role-play (mỗi case 1 type KH) để team Sale practice không?"

## Tone check

- ✅ Đồng nghiệp ngang hàng (không thấp giọng đi xin việc)
- ✅ Quy tắc 70/30 (KH 70%, Sale 30%)
- ✅ Câu hỏi mở > câu hỏi yes/no
- ❌ Không "anh/chị có muốn nghe em giới thiệu công ty không" (push pitch sớm)
