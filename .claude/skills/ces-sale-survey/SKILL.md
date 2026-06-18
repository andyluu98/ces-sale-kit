---
name: ces-sale-survey
description: Soạn form khảo sát KH B2B/B2C cho CES Global — pre-workshop, post-workshop, post-buổi-học, post-khóa, NPS. Dùng khi user nói "soạn form khảo sát", "gen survey KH", "khảo sát sau workshop", "/ces-sale-survey". Output Google Form spec + câu hỏi sẵn — Sale paste vào Form.
---

# CES Sale Survey — Form khảo sát KH

Skill gen câu hỏi survey theo 5 mục đích phổ biến. Output là **spec Google Form** (Sale chỉ cần copy-paste vào forms.google.com).

## Khi nào dùng

- Trước workshop: tuyển sinh + screening
- Sau workshop: feedback + lead qualification
- Sau buổi học khóa chính: feedback + thu thập case study
- Sau cả khóa: NPS + testimonial
- Khảo sát B2B trước in-house: pain assessment

## 5 type survey

| # | Type | Mục đích | Số câu | Khi gửi |
|---|---|---|---|---|
| 1 | **Pre-workshop** | Tuyển sinh + chuẩn bị đúng pain | 8-12 | Khi KH đăng ký form |
| 2 | **Post-workshop** | Feedback + lead qualification cho khóa chính | 6-10 | Cuối workshop / 24h sau |
| 3 | **Post-buổi-học** | Feedback nhanh từng buổi khóa | 4-6 | Cuối buổi |
| 4 | **Post-khóa (NPS)** | NPS + testimonial + case study | 10-15 | 1 tuần sau buổi cuối |
| 5 | **Pre-in-house B2B** | Pain assessment trước tailor curriculum | 12-18 | Sau buổi tư vấn đầu DN |

## Bước 1 — Hỏi đầu vào

```
1. Type survey? (1-5 từ bảng)
2. Đối tượng cụ thể? (B2C cá nhân / B2B nhân viên / B2B lãnh đạo)
3. Khóa/workshop nào? (lấy từ portfolio-khoa-ces.md)
4. Format thu thập? (a) Google Form · (b) Typeform · (c) Excel gửi email · (d) Phỏng vấn 1-1
5. Có cần Google Apps Script tự sinh form không? (vì hiện Chatbot HNH chưa hỗ trợ tự sinh — dùng Apps Script là cách CES đã chốt)
```

## Bước 2 — Tự đọc knowledge

- `knowledge/personas-khach-hang.md` — câu hỏi match persona
- `knowledge/portfolio-khoa-ces.md` — context khóa

## Bước 3 — Output spec Google Form

### Template Type 1 — Pre-workshop

```markdown
# Form đăng ký Workshop "{Tên workshop}" — CES Global

**Mô tả form:** "Cảm ơn anh/chị quan tâm Workshop. Em xin 2 phút để chuẩn bị buổi học phù hợp nhất — sẽ không gửi spam."

## Section 1: Thông tin cá nhân
1. Họ và tên * (short answer)
2. Email * (short answer, validation email)
3. SĐT / Zalo * (short answer)
4. Chức danh hiện tại * (short answer)
5. Công ty / tổ chức (short answer, optional)

## Section 2: Pain & nhu cầu
6. Anh/chị đang gặp khó khăn gì khi làm việc với [chủ đề workshop]? * (paragraph)
   - Vd: tốn 4h/bài content, không biết bắt đầu AI từ đâu...

7. Anh/chị đã thử công cụ AI nào chưa? (checkbox, multiple)
   - [ ] ChatGPT
   - [ ] Claude
   - [ ] Gemini
   - [ ] Copilot Microsoft
   - [ ] Chưa thử
   - [ ] Khác: ___

8. Mục tiêu sau workshop? * (multiple choice)
   - (a) Hiểu cơ bản để bắt đầu
   - (b) Áp dụng ngay vào công việc
   - (c) Đào tạo lại team
   - (d) Tìm hiểu khóa dài hơn

9. Biết Workshop qua đâu? * (multiple choice)
   - Facebook · LinkedIn · YouTube · Bạn giới thiệu · Website CES · Khác

## Section 3: Confirm
10. Anh/chị xác nhận tham gia đúng giờ {ngày + giờ workshop}? * (yes/no)
11. Có muốn nhận thêm ebook miễn phí trước workshop? (yes/no)

**Confirmation message:**
"Cảm ơn anh/chị đã đăng ký. Em sẽ gửi link Zoom + tài liệu chuẩn bị qua email trong 24h. — CES Global"
```

### Template Type 5 — Pre-in-house B2B

```markdown
# Khảo sát nhu cầu đào tạo AI — {Tên DN}

**Mô tả form:** "Khảo sát 5-7 phút giúp CES tailor chương trình 100% theo pain point DN anh/chị. Tất cả thông tin bảo mật."

## Section 1: Tổ chức
1. Tên DN + lĩnh vực *
2. Quy mô nhân sự * (multiple: <50, 50-200, 200-1000, >1000)
3. Số phòng ban tham gia đào tạo *
4. Người ra quyết định cuối cùng (vai trò) *

## Section 2: Pain hiện tại
5. 3 pain lớn nhất của DN cần AI giải quyết * (paragraph)
6. Phòng ban nào ưu tiên đào tạo trước? (checkbox)
7. Hiện đang dùng tool gì? * (paragraph)
8. Thử AI nội bộ chưa? Kết quả? * (paragraph)

## Section 3: Mục tiêu sau đào tạo
9. Output đo được sau 3 tháng anh/chị kỳ vọng * (paragraph)
10. Số nhân sự cần đào tạo (estimate) *
11. Hình thức ưu tiên * (online / offline tại DN / hybrid)
12. Thời gian dự kiến * (cuối tuần / giờ hành chính / tối)

## Section 4: Đầu tư
13. Ngân sách dự kiến * (multiple: <50tr, 50-200tr, 200-500tr, >500tr, chưa rõ)
14. Đã có vendor AI khác chưa? * (yes/no)
15. Timeline ra quyết định * (1 tuần / 2-4 tuần / 1-3 tháng / chưa rõ)

## Section 5: Liên hệ
16. Email người nhận proposal *
17. Tiện call lại vào khung giờ nào *

**Confirmation:**
"Em sẽ phân tích trong 48h và gửi đề xuất chi tiết. Cảm ơn anh/chị! — CES Global"
```

## Bước 4 — Google Apps Script (option)

Nếu user chọn "có cần Apps Script tự sinh form":

> "Em đề xuất pattern Apps Script đã chốt với HNH Travel — script đọc text mô tả → tạo Google Form auto. Em sinh code Apps Script luôn không?"

Nếu yes → gen Apps Script code mẫu (~30 dòng) deploy lên Google Drive.

## Sau khi có response

**Hỏi user:**
> "Form thu xong rồi, anh/chị muốn em phân tích response thành insight + lead score không? Em đọc Sheet → ra báo cáo top 10 lead nóng nhất."

→ Nếu yes, skill này có thể chuyển sang phân tích response.

## Tone check

- ✅ Câu hỏi NGẮN, không nhồi
- ✅ Required (*) chỉ field thật sự cần — < 50% câu là required
- ✅ Confirmation message ấm áp, không cứng
- ❌ Không hỏi thông tin nhạy cảm không cần (CMND, mức lương cá nhân)
- ❌ Không > 18 câu (KH sẽ bỏ giữa chừng)
