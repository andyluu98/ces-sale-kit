# Template — Báo giá CES Global

> Khung báo giá cho Skill `ces-sale-bao-gia`. Rõ ràng, không giấu phí.

```markdown
# BÁO GIÁ — {Tên khóa}
## CES Global × {Tên KH}

> Ngày: {YYYY-MM-DD}
> Hiệu lực: {YYYY-MM-DD} → {+30 ngày}
> Mã báo giá: BG-{YYMMDD}-{seq}

## Thông tin khóa
- **Tên:** {Tên khóa}
- **Số buổi:** {N} · **Thời lượng/buổi:** {giờ}h
- **Format:** {Online · Offline · Hybrid · In-house}
- **Đối tượng:** {từ portfolio}
- **Khai giảng dự kiến:** {YYYY-MM-DD}

## Chi tiết giá

| Hạng mục | Đơn giá | SL | Thành tiền |
|---|---|---|---|
| Học phí khóa | `{HOC_PHI}` | `{N HV}` | `{Tổng gross}` |
| **Tổng chưa ưu đãi** | | | **`{TONG_GROSS}`** |
| Ưu đãi `{LOAI}` | `-{X}%` | | `-{SO_TIEN_GIAM}` |
| **Tổng sau ưu đãi** | | | **`{TONG_NET}`** |
| VAT (10%) | | | `{VAT}` |
| **TỔNG THANH TOÁN** | | | **`{TONG_FINAL}`** |

## Bao gồm
- ✅ Tài liệu HV (PDF · slide · file thực hành)
- ✅ Truy cập LMS Academy 6 tháng
- ✅ Repo công khai + cộng đồng 1.200+ thành viên
- ✅ Hỗ trợ sau khóa 6 tháng
- ✅ Chứng chỉ hoàn thành CES Global

## Không bao gồm
- ❌ Phí tool 3rd party (ChatGPT Plus $20/tháng · Claude Pro $20/tháng — nếu khóa yêu cầu)
- ❌ Phí công tác nếu in-house ngoài Hà Nội
- ❌ Customize curriculum sâu (báo giá riêng)

## Điều kiện thanh toán

**Phương thức:** {1 đợt · 2 đợt 50-50 · 3 đợt 40-30-30}

| Đợt | % | Thời hạn | Số tiền |
|---|---|---|---|
| 1 | 50% | Ngay khi xác nhận | `{}` |
| 2 | 50% | Trước KG 7 ngày | `{}` |

**Tài khoản nhận:**
- CTCP Công nghệ Trí tuệ Nhân tạo CES Global
- STK: `{STK}` · `{Ngân hàng}`
- Nội dung CK: "{Tên KH} - {Tên khóa}"

**Xuất hóa đơn:**
- Đơn vị: `{tên DN}`
- MST: `{MST}`
- Địa chỉ: `{địa chỉ}`

## Cam kết
- HV cuối khóa build được {3-5 use case} cụ thể
- Buổi bổ sung miễn phí nếu HV chưa đạt
- Hỗ trợ 6 tháng sau khóa

## Liên hệ
{Sale name} — {SĐT} — {Email}
CES Global · 222 Nguyễn Văn Tuyết, Đống Đa, HN

> *"Kinh doanh hiệu quả — Phát triển bền vững."*
```

## Lưu ý

- **Hiệu lực 30 ngày** — sau đó cần gen lại
- **STK CES** — hỏi Linh (Phụ trách Sale) số chính thức
- **MST CES Global** — fill vào knowledge sau khi anh Tiệp confirm
