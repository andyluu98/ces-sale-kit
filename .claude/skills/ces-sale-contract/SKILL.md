---
name: ces-sale-contract
description: Soạn hợp đồng đào tạo AI cho CES Global — hợp đồng nguyên tắc, dịch vụ, in-house, coaching. Dùng khi user nói "soạn hợp đồng cho KH [X]", "gen contract khóa [Y]", "/ces-sale-contract". Output hợp đồng markdown — Sale review, gửi pháp chế CES duyệt rồi ký.
---

# CES Sale Contract — Hợp đồng đào tạo

Skill gen hợp đồng đào tạo. **CẢNH BÁO:** Output là draft — phải gửi pháp chế CES (anh Tiệp/A.Linh) review trước khi ký.

## Khi nào dùng

- KH B2B chốt deal, cần hợp đồng dịch vụ
- KH cá nhân/B2C đăng ký khóa lớn (>50tr), cần hợp đồng nguyên tắc
- In-house custom DN — luôn cần hợp đồng

## 4 loại hợp đồng

| # | Loại | Khi dùng |
|---|---|---|
| 1 | **Hợp đồng nguyên tắc** | KH B2B định ký long-term, ký lần đầu |
| 2 | **Hợp đồng dịch vụ đào tạo** | Mỗi khóa public/in-house cụ thể |
| 3 | **Phụ lục hợp đồng** | Đã có hợp đồng nguyên tắc, thêm khóa mới |
| 4 | **Thỏa thuận coaching 1-1** | Coaching founder/CEO |

## Bước 1 — Hỏi đầu vào

```
1. Loại hợp đồng? (1-4)
2. Bên A (KH)? Tên đầy đủ DN + MST + địa chỉ + người đại diện ký
3. Bên B (CES Global) — em fill sẵn từ knowledge/brand
4. Khóa/dịch vụ cụ thể? (lấy từ portfolio)
5. Giá trị hợp đồng + cách thanh toán?
6. Thời gian thực hiện? (KG → kết thúc)
7. Đã có hợp đồng nguyên tắc trước chưa? (nếu type 3)
```

## Bước 2 — Tự đọc knowledge

- `knowledge/brand-ces-global.md` — thông tin pháp lý CES
- `knowledge/portfolio-khoa-ces.md` — chi tiết khóa
- `templates/contract-template.md` — khung hợp đồng

## Bước 3 — Output hợp đồng (cấu trúc 8 điều)

```markdown
# HỢP ĐỒNG DỊCH VỤ ĐÀO TẠO AI
**Số:** HĐ-CES-{YYMMDD}-{seq}/{Tên DN}

> Hà Nội, ngày {DD} tháng {MM} năm {YYYY}

## CĂN CỨ

- Bộ luật Dân sự 2015
- Luật Thương mại 2005
- Nhu cầu của hai Bên

## BÊN A (KHÁCH HÀNG)

- **Tên đơn vị:** {Tên DN}
- **Mã số thuế:** {MST}
- **Địa chỉ:** {Địa chỉ trụ sở}
- **Đại diện:** {Tên} — {Chức vụ}
- **Điện thoại:** {SĐT} · **Email:** {Email}

## BÊN B (CES GLOBAL)

- **Tên đầy đủ:** Công ty Cổ phần Công nghệ Trí Tuệ Nhân Tạo CES Global
- **Mã số thuế:** {MST_CES}
- **Địa chỉ:** 222 Nguyễn Văn Tuyết, Đống Đa, Hà Nội
- **Đại diện:** {Tên anh Tiệp} — Tổng Giám đốc
- **Điện thoại:** 0911 991 288 · **Email:** cesglobal.ai@gmail.com

---

## ĐIỀU 1 — NỘI DUNG DỊCH VỤ

Bên B cung cấp cho Bên A chương trình đào tạo:

- **Khóa:** {Tên khóa}
- **Số buổi:** {N} · **Thời lượng/buổi:** {giờ}h
- **Format:** {Online / Offline tại {địa điểm} / Hybrid / In-house tại Bên A}
- **Đối tượng:** {Mô tả HV} — Số lượng dự kiến: {N HV}
- **Khai giảng:** {YYYY-MM-DD} · **Kết thúc dự kiến:** {YYYY-MM-DD}

**Bao gồm:**
- (a) Tài liệu HV: slide, PDF bài giảng, file thực hành
- (b) Truy cập LMS Academy 6 tháng
- (c) Repo công khai + cộng đồng CES Academy
- (d) Hỗ trợ sau khóa 6 tháng (Q&A inbox/email)
- (e) Chứng chỉ hoàn thành CES Global

## ĐIỀU 2 — GIÁ TRỊ HỢP ĐỒNG

- **Học phí:** {HOC_PHI_GROSS} VNĐ (chưa VAT)
- **Ưu đãi:** -{X}% = -{SO_TIEN} VNĐ
- **Học phí sau ưu đãi:** {HOC_PHI_NET} VNĐ
- **VAT (10%):** {VAT} VNĐ
- **TỔNG THANH TOÁN:** **{TONG_FINAL} VNĐ**
- *Bằng chữ:* {viết bằng chữ}

## ĐIỀU 3 — THANH TOÁN

**Phương thức:** Chuyển khoản.

**Lịch thanh toán:**

| Đợt | % | Số tiền | Thời hạn |
|---|---|---|---|
| 1 | 50% | {} | Trong 7 ngày sau khi ký HĐ |
| 2 | 50% | {} | Trước KG 7 ngày |

**Tài khoản nhận:**
- CTCP Công nghệ Trí tuệ Nhân tạo CES Global
- STK: {STK} · {Ngân hàng}
- Nội dung: "TT HĐ {số HĐ} - {Tên Bên A}"

**Hóa đơn VAT:** Bên B xuất hóa đơn cho từng đợt thanh toán trong 5 ngày làm việc sau khi nhận tiền.

## ĐIỀU 4 — QUYỀN VÀ NGHĨA VỤ BÊN A

**Quyền:**
- Nhận đầy đủ dịch vụ theo Điều 1
- Yêu cầu tài liệu trước KG
- Được hỗ trợ 6 tháng sau khóa

**Nghĩa vụ:**
- Thanh toán đúng hạn (Điều 3)
- Cử HV tham gia ≥ 80% buổi học
- Cung cấp thông tin DN + phản hồi để Bên B tailor (in-house)

## ĐIỀU 5 — QUYỀN VÀ NGHĨA VỤ BÊN B

**Quyền:**
- Nhận thanh toán đúng hạn
- Sử dụng case study Bên A (sau khi xin phép)

**Nghĩa vụ:**
- Cung cấp dịch vụ đúng nội dung Điều 1
- Đảm bảo chất lượng GV + tài liệu
- Hỗ trợ sau khóa 6 tháng
- Bảo mật thông tin Bên A

## ĐIỀU 6 — CHẤT LƯỢNG & CAM KẾT ĐẦU RA

Bên B cam kết:
- HV cuối khóa build được {3-5 use case} thực tế
- Nếu < 80% HV không đạt cam kết → Bên B tổ chức **buổi bổ sung miễn phí**
- Bảo hành kỹ thuật 6 tháng sau khóa

## ĐIỀU 7 — BẢO MẬT

- Hai Bên cam kết bảo mật thông tin của nhau trong và sau khi thực hiện HĐ
- Thời hạn bảo mật: 3 năm sau khi HĐ kết thúc
- Vi phạm bảo mật: bồi thường thiệt hại thực tế

## ĐIỀU 8 — TRANH CHẤP & ĐIỀU KHOẢN CHUNG

- Hai Bên ưu tiên thương lượng. Không thương lượng được → giải quyết tại Tòa án có thẩm quyền tại Hà Nội
- HĐ có hiệu lực từ ngày ký, kéo dài đến khi hoàn thành nghĩa vụ hai Bên
- HĐ làm thành 02 bản, mỗi Bên giữ 01 bản, có giá trị pháp lý như nhau

---

## ĐẠI DIỆN BÊN A                    ĐẠI DIỆN BÊN B

(Ký + đóng dấu)                      (Ký + đóng dấu)


{Tên Bên A}                          {Tên anh Tiệp}
```

## Bước 4 — Cảnh báo bắt buộc

Sau khi gen, output kèm warning:

> ⚠️ **HỢP ĐỒNG NÀY LÀ DRAFT.** Trước khi ký phải:
> 1. Gửi pháp chế CES (anh Tiệp + A. Linh) review
> 2. Verify MST + STK + đại diện ký 2 bên
> 3. In bản chính thức, đóng dấu

## Lưu file

Default: `outputs/contract-{type}-{YYMMDD}-{kh-slug}.md`

Sau review pháp chế → convert sang Word brand CES (dùng skill `office-docs` hoặc `ces-training-curriculum`).

## Anti-patterns

| ❌ Sai | ✅ Đúng |
|---|---|
| Gửi thẳng KH không review pháp chế | LUÔN review pháp chế trước |
| Cam kết "thành công 100%" trong Điều 6 | "Build được {N} use case cụ thể + buổi bổ sung miễn phí" |
| Quên Điều bảo mật | Điều 7 bắt buộc cho B2B |
| MST/STK sai → KH không CK được | Verify trước khi gửi |
