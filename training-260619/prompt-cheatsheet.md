# Cheat Sheet Prompt cho Sale CES Global

> In 1 trang để Sale cầm theo dùng hàng ngày. 20 prompt + 8 invocation skill.

## A. Invocation Skill (gõ trực tiếp trong Claude Code)

| Gõ | Output |
|---|---|
| `/ces-sale-de-xuat` | Skill hỏi 6 câu → gen proposal 8 phần |
| `/ces-sale-bao-gia` | Skill hỏi 6 câu → gen báo giá bảng |
| `/ces-sale-kich-ban` | Skill hỏi 6 câu → gen kịch bản tư vấn 5 phần |
| `/ces-sale-email` | Skill hỏi type email → gen email 8 type |
| `/ces-sale-xu-ly-tu-choi` | Skill hỏi objection KH → script trả lời + evidence |
| `/ces-sale-khao-sat` | Skill hỏi type survey → spec Google Form |
| `/ces-sale-hop-dong` | Skill hỏi loại HĐ → hợp đồng draft 8 điều |

---

## B. 20 Prompt mẫu — Sale paste vào Claude.ai/Claude Code

### Nhóm 1: Soạn proposal/báo giá (5 prompt)

**1. Proposal cho B2B:**
```
Soạn proposal khóa {Tên khóa} cho {Tên DN},
persona {P1-Founder/P2-CMO/P3-HRM/P4-CTO},
ngành {ngành}, quy mô {N} người,
pain chính: {1-3 ý}.
Format theo brand CES Global, có placeholder học phí.
```

**2. Proposal cho B2C (cá nhân):**
```
Soạn proposal khóa {X} cho cá nhân:
{tên KH}, {chức danh}, đã dùng AI: {ChatGPT/Claude/chưa},
mục tiêu: {pain cụ thể}.
Brand CES, 1 trang, có CTA đặt demo.
```

**3. Báo giá nhanh:**
```
Báo giá khóa {X}, {N} HV, ưu đãi {Z}%,
thanh toán 2 đợt 50-50.
Bao gồm + không bao gồm rõ ràng.
```

**4. Báo giá in-house DN lớn:**
```
Báo giá in-house khóa {X} cho {DN}, {N} nhân sự,
{ngày}, tại Hà Nội/HCM, có công tác phí GV.
Brand CES, có cam kết đầu ra.
```

**5. So sánh 3 phương án giá:**
```
KH ngân sách {Y}tr, gen 3 phương án:
- Cơ bản: 1 khóa public
- Trung: khóa + coaching 2 buổi
- Cao: in-house tailor 100%
Mỗi phương án + ROI dự kiến.
```

### Nhóm 2: Kịch bản & gọi điện (4 prompt)

**6. Cold call 10 phút:**
```
Kịch bản cold call 10 phút cho KH {tên},
persona {P}, ngành {X},
mục tiêu: đặt demo 30 phút.
Bao hook + 5 câu discovery + closing nhẹ.
```

**7. Kịch bản gặp face-to-face 60 phút:**
```
Kịch bản gặp cafe 60' với KH {tên}, persona {P}.
Mục tiêu: pitch khóa + chốt proposal.
70% KH nói, 30% mình nói. Quy tắc CES.
```

**8. Follow-up gọi sau proposal:**
```
Kịch bản gọi follow-up 5 phút,
KH {tên} đã nhận proposal 3 ngày trước, chưa rep.
Tone nhẹ, không push, mục tiêu lấy feedback.
```

**9. Kịch bản chốt deal:**
```
KH {tên} đã OK giá, đang chần chừ ký HĐ.
Kịch bản closing 15 phút, đưa ra 2 option:
ký ngay (có ưu đãi) hoặc tuần sau (giá thường).
Tone CES — không ép.
```

### Nhóm 3: Email (4 prompt)

**10. Email cold:**
```
Email cold gửi {tên}, {chức vụ} tại {DN ngành X}.
Subject + body <100 từ + CTA đặt 15 phút call.
Có hook giá trị cụ thể (case study DN cùng ngành).
```

**11. Email sau proposal:**
```
Email gửi kèm proposal cho KH {tên} sau buổi gọi.
Tóm tắt 3 ý pain KH chia sẻ + đề xuất + bước tiếp.
< 150 từ, có CTA.
```

**12. Email follow-up 3 ngày KH chưa rep:**
```
Email follow-up KH {tên} 3 ngày chưa rep sau proposal.
Tone nhẹ, không guilt-trip, < 60 từ.
CTA: hỏi có cần làm rõ điểm nào.
```

**13. Email closing chốt deal:**
```
Email gửi hợp đồng + STK cho KH {tên} đã OK ký.
Có: link HĐ, STK CES, nội dung chuyển khoản,
hóa đơn xuất khi nào, bước tiếp theo sau thanh toán.
```

### Nhóm 4: Xử lý objection (4 prompt)

**14. Objection "bên nào cũng chạy Claude":**
```
KH nói: "Bên nào cũng dạy Claude, sao phải học CES?"
Persona 5 (1 person company).
Script trả lời theo tone CES (không hạ thấp đối thủ).
Kèm evidence cụ thể.
```

**15. Objection "giá cao":**
```
KH so giá: "Khóa kia X triệu, CES gấp 2."
Trả lời theo USP CES — không cạnh tranh giá,
quy về ROI 6 tháng. Có bảng so sánh giá trị.
```

**16. Objection "tự học YouTube được":**
```
KH nói: "Tôi tự xem YouTube AI 6 tháng rồi,
sao phải mất tiền học CES?"
Trả lời: bán LỘ TRÌNH + người dẫn + sản phẩm cuối.
```

**17. Objection "đội tôi không biết code":**
```
KH lo team không kỹ thuật học AI không nổi.
Trả lời: 90% khóa CES là no-code, có case AI Teen
(học sinh 12 tuổi build chatbot).
```

### Nhóm 5: Survey & phân tích (3 prompt)

**18. Survey pre-workshop:**
```
Soạn Google Form đăng ký Workshop {tên},
10 câu, có pain assessment + ngân sách.
Confirmation message ấm áp.
```

**19. Survey pre-in-house B2B:**
```
Khảo sát nhu cầu đào tạo AI cho DN {tên},
18 câu, 5 section (tổ chức · pain · mục tiêu · đầu tư · liên hệ).
Format Google Form spec.
```

**20. Phân tích response form:**
```
Đây là response Google Form Workshop {tên} ({N} lead).
Phân tích: top 3 pain · 5 lead nóng nhất · gợi ý khóa upsell.
Output bảng + script gọi mỗi lead.
```

---

## C. Quy tắc nhanh khi prompt

✅ **NÊN:**
- Bắt đầu bằng động từ ("Soạn", "Gen", "Phân tích")
- Cung cấp context: persona + ngành + quy mô + ngân sách
- Chỉ định format output ("bảng", "5 phần", "< 200 từ")
- Yêu cầu brand: "theo tone CES Global"

❌ **TRÁNH:**
- "Giúp em với khách này" (quá chung)
- "Soạn proposal đẹp đẹp" (không đo được)
- Không nói persona → output generic
- "Đảm bảo thắng deal 100%" (không cam kết được)

---

## D. Khi Skill output chưa ưng

**Refine 3 vòng tối đa:**

1. **Vòng 1:** "Output ngắn quá / dài quá. Làm lại {200 từ}."
2. **Vòng 2:** "Phần X chưa khớp persona. Sửa: {chi tiết}."
3. **Vòng 3:** "OK, fix nốt {1 câu}."

→ Sau 3 vòng vẫn chưa OK → vào Skill knowledge edit trực tiếp + báo Hải.

---

## E. Skill knowledge — biết edit khi cần

| File | Khi cần edit |
|---|---|
| `knowledge/portfolio-khoa-ces.md` | Có khóa mới · học phí thay đổi · KH mới |
| `knowledge/personas-khach-hang.md` | Gặp persona mới chưa có trong 5 |
| `knowledge/objection-bank.md` | Gặp objection mới ngoài 12 cái |
| `knowledge/brand-ces-global.md` | Brand voice update (1 năm 1 lần) |

→ Edit xong commit + push GitHub → cả team có ngay.

---

**In 1 trang, dán lên bàn. Dùng hàng ngày.**
