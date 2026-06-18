---
name: ces-sale-objection
description: Xử lý objection KH khi tư vấn khóa CES. Dùng khi user nói "KH nói X, trả lời sao", "objection [...] làm gì", "/ces-sale-objection". Skill tự đọc objection-bank → đưa script phản hồi theo 4 trụ CES + evidence cụ thể.
---

# CES Sale Objection Handler

Skill trả lời objection KH theo workflow: **Lặp lại → Hỏi sâu → Cô lập → Trả lời → Confirm**. Không đối đầu, không né.

## Khi nào dùng

- Buổi gọi/gặp KH đang diễn ra, KH nêu khúc mắc
- Sale chuẩn bị gặp KH, muốn xem trước objection có thể gặp
- Sale review case "KH nói X, mình trả lời thế nào tốt hơn"

## Bước 1 — Hỏi đầu vào

```
1. Objection KH nguyên văn là gì? (paste câu KH nói)
2. Context: đây là buổi gọi cold / warm / sau proposal / sau báo giá?
3. Persona KH? (1-5)
4. KH nói tone như nào? (a) Lịch sự nhẹ · (b) Hơi gắt · (c) So sánh với đối thủ cụ thể · (d) Né để kết thúc gọi
```

## Bước 2 — Tự đọc knowledge

- `knowledge/objection-bank.md` — 12 objection có script sẵn
- `knowledge/usp-vs-competitor.md` — USP để chèn vào phản hồi
- `knowledge/personas-khach-hang.md` — match tone persona

## Bước 3 — Match objection

**Nếu objection nằm trong 12 cái có sẵn:**
→ Output script từ bank + customize theo context + persona.

**Nếu objection MỚI (không có trong bank):**
→ Theo workflow 5 bước:

### Workflow 5 bước cho objection mới

1. **Lặp lại** (1 câu — để KH thấy mình hiểu):
   > "Em hiểu — anh/chị đang lo về [tóm tắt 1 câu]."

2. **Hỏi sâu** (1 câu — bóc lớp ý ẩn):
   > "Em muốn hiểu thêm — điều gì khiến anh/chị nghĩ vậy ạ?"

3. **Cô lập** (1 câu — chắc đây là khúc mắc duy nhất):
   > "Ngoài [điểm này] còn gì làm anh/chị do dự nữa không?"

4. **Trả lời** (3-5 câu — theo 4 trụ CES):
   - Chuyên nghiệp: có số liệu/case study
   - Tiên phong: định vị AI First
   - Thực chiến: chỉ ra kết quả đo được
   - Nhân văn: không đối đầu

5. **Confirm** (1 câu — đảm bảo đã giải đáp):
   > "Em đã giải đáp được điểm này chưa, hay anh/chị cần thêm gì?"

## Bước 4 — Output

```markdown
## Phản hồi objection: "{nguyên văn KH}"

### Phân tích
- **Ý ẩn:** {KH thật sự lo gì}
- **Persona context:** {persona N có hay gặp objection này không}
- **Tone match:** {nhẹ / vừa / mạnh}

### Script trả lời (đọc lên dùng được)

> {Script 3-5 câu theo 5 bước trên}

### Evidence kèm
- Case study: {tên DN tương tự}
- Số liệu: {ROI / outcome đo được}
- Link: {repo / website / video}

### Bước tiếp theo nếu KH OK
- {Đặt demo / gửi proposal / call back}

### Bước tiếp theo nếu KH vẫn từ chối
- KHÔNG push lần 3
- Lùi 1 bước: "Em hiểu — em note lại để gọi anh/chị Q3, lúc đó mình review lại nhé"
- Gửi value miễn phí (ebook · case study) để giữ kết nối
```

## Top objection nhanh

| KH nói | Quick response |
|---|---|
| "Bên nào cũng chạy Claude" | Khác biệt: hệ sinh thái + cộng đồng + repo public |
| "Giá cao" | So ROI 6 tháng, không so giá khóa |
| "Tự học được YouTube" | Bán LỘ TRÌNH + người dẫn, không bán video |
| "Học xong không áp dụng" | In-house custom theo phòng ban |
| "Đội tôi không biết code" | 90% khóa public là no-code |
| "Cho tôi suy nghĩ" | Gửi 3 thứ tham khảo + call lại sau 3 ngày |

→ Chi tiết script + evidence: `knowledge/objection-bank.md`

## Anti-patterns

| ❌ Sai | ✅ Đúng |
|---|---|
| "Không, anh/chị nhầm rồi..." | "Em hiểu — anh/chị đang lo về..." |
| Hạ thấp đối thủ | Nhận họ có ưu điểm, chỉ ra khác biệt |
| Pitch giá ngay khi KH chê giá cao | Quy về ROI 6 tháng |
| Push 3 lần liên tiếp | Push max 2 lần, sau đó lùi |
| Cam kết "100% thành công" | "Cam kết HV build được {3 use case} cụ thể" |

## Khi gặp objection mới (chưa có trong bank)

**Sau buổi gọi, làm 2 việc:**
1. Note lại nguyên văn + context
2. PR vào `knowledge/objection-bank.md` để team dùng chung

→ Bank này là tài sản chung — càng nhiều objection được lưu, Sale càng đỡ phải suy nghĩ lại.
