---
name: ces-sale-quote
description: Soạn bảng báo giá CES Global cho khóa đào tạo AI. Dùng khi user nói "soạn báo giá", "gen báo giá cho khách [X]", "báo giá khóa [tên]", "/ces-sale-quote". Output bảng báo giá rõ ràng — học phí · ưu đãi · thanh toán · không bao gồm — chuẩn brand CES.
---

# CES Sale Quote — Báo giá chuẩn brand

Skill gen bảng báo giá Sale gửi KH. Khác proposal: báo giá NGẮN GỌN, chỉ tập trung số tiền + điều kiện thanh toán.

## Khi nào dùng

- KH yêu cầu "anh/chị gửi báo giá cho em"
- Sau khi proposal đã gửi, KH xác nhận muốn xem giá cụ thể
- KH so giá với đối thủ, cần bảng so sánh

## Bước 1 — Hỏi đầu vào

```
1. Khóa nào? (chọn từ portfolio-khoa-ces.md hoặc custom)
2. Số HV?
3. Format? (online · offline · hybrid · in-house tại DN)
4. Có thuộc đối tượng ưu đãi không? (a) Early bird · (b) HV cũ · (c) Nhóm ≥5 · (d) Đối tác · (e) Không
5. Thanh toán? (a) 1 đợt · (b) 2 đợt 50/50 · (c) 3 đợt
6. Xuất hóa đơn? Tên đơn vị · MST · địa chỉ
```

## Bước 2 — Tự đọc knowledge

- `knowledge/portfolio-khoa-ces.md` — học phí khóa (placeholder)
- `knowledge/brand-ces-global.md` — format + tone

## Bước 3 — Output báo giá

```markdown
# BÁO GIÁ — {Tên khóa}
## CES Global × {Tên KH}

> Ngày: {YYYY-MM-DD}
> Hiệu lực: {YYYY-MM-DD} → {YYYY-MM-DD} (30 ngày)
> Mã báo giá: BG-{YYMMDD}-{seq}

## Thông tin khóa
- **Tên:** {Tên khóa}
- **Số buổi:** {N} · **Thời lượng/buổi:** {giờ}h
- **Format:** {Online/Offline/Hybrid/In-house}
- **Đối tượng:** {từ portfolio}
- **Khai giảng dự kiến:** {YYYY-MM-DD}

## Chi tiết giá

| Hạng mục | Đơn giá | SL | Thành tiền |
|---|---|---|---|
| Học phí khóa | {HOC_PHI} | {N HV} | {HOC_PHI × N} |
| **Tổng chưa ưu đãi** | | | **{TONG_GROSS}** |
| Ưu đãi {LOAI_UU_DAI} | -{X}% | | -{SO_TIEN_GIAM} |
| **Tổng sau ưu đãi** | | | **{TONG_NET}** |
| VAT (10%) | | | {VAT} |
| **TỔNG THANH TOÁN** | | | **{TONG_FINAL}** |

## Bao gồm
- ✅ Tài liệu HV (PDF · slide · file thực hành)
- ✅ Truy cập LMS Academy 6 tháng (academy.cesglobal.com.vn)
- ✅ Repo công khai + cộng đồng 1.200+ thành viên
- ✅ Hỗ trợ sau khóa 6 tháng (Q&A inbox/email)
- ✅ Chứng chỉ hoàn thành CES Global

## Không bao gồm
- ❌ Phí tool 3rd party (ChatGPT Plus 20$/tháng, Claude Pro 20$/tháng — nếu khóa yêu cầu)
- ❌ Phí công tác nếu in-house ngoài Hà Nội (di chuyển + lưu trú GV)
- ❌ Customize curriculum sâu (báo giá riêng nếu cần)

## Điều kiện thanh toán

**Phương thức:** {1 đợt / 2 đợt 50-50 / 3 đợt 40-30-30}

| Đợt | % | Thời hạn | Số tiền |
|---|---|---|---|
| 1 | 50% | Ngay khi xác nhận đăng ký | {} |
| 2 | 50% | Trước KG 7 ngày | {} |

**Tài khoản nhận:**
- CTCP Công nghệ Trí tuệ Nhân tạo CES Global
- STK: {STK} · {Ngân hàng}
- Nội dung CK: "{Tên KH} - {Tên khóa}"

**Xuất hóa đơn:**
- Đơn vị: {tên DN từ input}
- MST: {MST}
- Địa chỉ: {địa chỉ}

## Cam kết
- HV cuối khóa build được {3-5 use case} cụ thể
- Buổi bổ sung miễn phí nếu HV chưa đạt
- Hỗ trợ kỹ thuật 6 tháng sau khóa

## Liên hệ
{Sale name} — {SĐT} — {Email}
CES Global · 222 Nguyễn Văn Tuyết, Đống Đa, HN

> *"Kinh doanh hiệu quả — Phát triển bền vững."*
```

## Bước 4 — Output thêm (option)

Sau khi trả markdown, hỏi user:
> "Anh/chị muốn em export Excel để gửi KH không? (em sẽ gen file `quote-{date}-{slug}.xlsx`)"

Nếu yes → dùng skill `office-docs` hoặc Windows-MCP để gen Excel.

## Tone check

- ✅ Bảng rõ, không giấu phí
- ✅ "Không bao gồm" minh bạch
- ✅ Hạn báo giá rõ (30 ngày)
- ✅ Có STK + thông tin xuất hóa đơn
- ❌ Không "giảm giá sốc 50%" — báo giá chuyên nghiệp không sale theo MKT
