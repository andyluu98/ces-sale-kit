---
name: ces-sale-email
description: Soạn email Sale CES Global — cold outreach, warm follow-up, closing, nurture. Dùng khi user nói "soạn email gửi KH [X]", "viết email follow-up", "email closing", "/ces-sale-email". Output email chuẩn brand, 8 template chính + custom.
---

# CES Sale Email — Email gửi KH chuẩn brand

Skill gen email Sale theo 8 type phổ biến. Ngắn, có CTA rõ, đúng tone CES.

## Khi nào dùng

- Sale chuẩn bị gửi email cho KH (cold/warm/closing/nurture)
- Cần follow-up sau buổi gọi/gặp
- Gửi proposal/báo giá kèm email cover

## 8 type email

| # | Type | Khi dùng |
|---|---|---|
| 1 | **Cold outreach** | KH chưa biết CES, lần đầu gửi |
| 2 | **Warm follow-up sau form** | KH đăng ký workshop/form, follow-up |
| 3 | **Sau buổi gọi đầu** | Gửi tóm tắt + bước tiếp |
| 4 | **Gửi proposal** | Cover email cho file proposal |
| 5 | **Gửi báo giá** | Cover email cho báo giá + STK |
| 6 | **Follow-up sau proposal** (3 ngày) | KH chưa rep |
| 7 | **Closing — chốt deal** | KH OK giá, chốt thanh toán + hợp đồng |
| 8 | **Nurture — KH chưa sẵn sàng** | Long-term, gửi value miễn phí |

## Bước 1 — Hỏi đầu vào

```
1. Type email? (1-8 từ bảng trên)
2. KH là ai? Tên + persona + chức danh
3. Context cụ thể: KH đã làm gì với CES rồi? (đăng ký form / gọi / gặp / nhận proposal)
4. Mục tiêu email này? (đặt demo / chốt giá / chốt deal / giữ liên lạc)
5. CTA mong muốn? (a) Rep lại email · (b) Đặt lịch call · (c) Click link đăng ký · (d) Thanh toán
```

## Bước 2 — Tự đọc knowledge

- `knowledge/brand-ces-global.md` — tone email
- `knowledge/personas-khach-hang.md` — ngôn ngữ persona
- `templates/email-templates.md` — 8 template cơ bản

## Bước 3 — Output email (cấu trúc 5 phần)

```markdown
**Subject:** [{type}] {nội dung cụ thể} — CES Global

**Pre-header:** {1 câu 80-100 ký tự hiển thị bên cạnh subject trong inbox}

---

Kính gửi {Anh/Chị + Tên},

**[Mở đầu — 1-2 câu]**
{Hook ngắn: nhắc context KH đã làm với CES + lý do gửi email này}

**[Thân — 2-4 câu]**
{Giá trị cụ thể em mang lại: case study / demo / tài liệu / link / proposal}

**[CTA — 1-2 dòng]**
{Action cụ thể: "Anh/chị xem qua giúp em..." / "Em đặt lịch call 30' tuần này được không?"}

**[Kết — 1 câu]**
{Câu kết ấm áp, không "trân trọng" cứng}

Em cảm ơn anh/chị.

---
**{Sale name}** — Phòng Kinh doanh
📞 {SĐT} · 📧 {Email}
**CES Global** · www.cesglobal.com.vn
*"Đồng hành chuyển đổi AI cùng doanh nghiệp."*
```

## 8 Subject template

| Type | Subject mẫu |
|---|---|
| 1 Cold | "{Tên KH} – 3 phút về AI cho ngành {ngành}" |
| 2 Warm | "Cảm ơn anh/chị đã đăng ký Workshop {tên} — bước tiếp theo" |
| 3 Sau gọi | "Tóm tắt buổi nói chuyện hôm nay + 2 file gửi anh/chị" |
| 4 Proposal | "Đề xuất chương trình AI cho {DN} — file đính kèm" |
| 5 Báo giá | "Báo giá khóa {tên} — hiệu lực 30 ngày" |
| 6 Follow-up | "Anh/chị có thắc mắc gì về đề xuất em gửi không ạ?" |
| 7 Closing | "Hợp đồng khóa {tên} + STK thanh toán" |
| 8 Nurture | "Tặng anh/chị ebook: {tên ebook} — không có ý gì khác đâu ạ" |

## Tone check theo type

- **Cold:** Ngắn (< 100 từ), hook giá trị cụ thể, không pitch ngay
- **Warm/Sau gọi:** Trung bình (100-150 từ), nhắc context, CTA rõ
- **Proposal/Báo giá:** Cover ngắn (~80 từ), file là chính
- **Follow-up:** Cực ngắn (< 60 từ), không guilt-trip
- **Closing:** Rõ ràng (100-150 từ), có STK + bước tiếp theo
- **Nurture:** Giá trị thuần (ebook/case study), không push

## Anti-patterns

| ❌ Sai | ✅ Đúng |
|---|---|
| "Kính gửi quý khách hàng" | "Kính gửi anh/chị {tên}" |
| Subject "Đề xuất hợp tác từ CES Global" (chung chung) | "Đề xuất chương trình AI cho {DN} — file đính kèm" |
| Email 500 từ dài dòng | < 200 từ, có bullet, có CTA |
| Không có CTA | Action cụ thể trong 1-2 dòng |
| "Trân trọng, [tên]" cuối | "Em cảm ơn anh/chị" + signature đầy đủ |
| Cold mà giới thiệu công ty 3 đoạn | Cold = 1 hook + 1 giá trị + 1 CTA |

## Bước 4 — Output thêm

Sau khi gen email, hỏi:
> "Anh/chị có muốn em gen 3 version A/B/C để test subject line nào mở nhiều hơn không?"

## Lưu

Default: trả markdown trong chat (ready-to-paste vào Gmail/Outlook).

Nếu user yêu cầu lưu file: `outputs/email-{type}-{YYMMDD}-{kh-slug}.md`
