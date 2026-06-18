---
name: ces-sale-proposal
description: Soạn proposal CES Global gửi KH B2B/B2C sau buổi tư vấn đầu. Dùng khi user nói "soạn proposal", "viết đề xuất khóa", "gen proposal cho khách [X]", "/ces-sale-proposal". Skill tự đọc persona + portfolio + brand → output proposal markdown chuẩn brand CES, có placeholder học phí để Sale fill.
---

# CES Sale Proposal — Soạn proposal chuẩn brand

Skill gen proposal Sale gửi KH sau buổi tư vấn đầu. Output là markdown đầy đủ — Sale chỉ fill học phí + tên KH + 1-2 detail cá nhân hóa rồi gửi.

## Khi nào dùng

- Sau buổi tư vấn đầu, KH muốn xem chi tiết bằng văn bản
- KH yêu cầu "gửi em file đề xuất"
- Sale chuẩn bị gặp KH lần 2, cần proposal làm anchor

## Bước 1 — Hỏi đầu vào (gom 1 lượt)

```
1. KH là ai? Tên DN/cá nhân + lĩnh vực
2. Persona nào? (1) Founder/CEO · (2) CMO · (3) HRM · (4) CTO · (5) Cá nhân tự doanh
3. Loại đào tạo? (a) Khóa public · (b) In-house custom · (c) Coaching 1-1 · (d) Workshop
4. Pain point chính KH đã chia sẻ (1-2 ý)
5. Quy mô KH? (số người tham gia / phòng ban / cá nhân)
6. Ngân sách dự kiến? (a) <50tr · (b) 50-200tr · (c) 200-500tr · (d) >500tr · (e) Chưa rõ
```

## Bước 2 — Tự đọc knowledge

LUÔN đọc:
- `knowledge/brand-ces-global.md` — tone + tagline + cấu trúc
- `knowledge/portfolio-khoa-ces.md` — khóa nào fit persona/pain
- `knowledge/personas-khach-hang.md` — ngôn ngữ persona
- `knowledge/usp-vs-competitor.md` — USP để chèn vào

## Bước 3 — Output proposal (cấu trúc 8 phần)

```markdown
# ĐỀ XUẤT CHƯƠNG TRÌNH ĐÀO TẠO AI
## CES Global × {Tên KH}

> Gửi: {Người nhận} · {Vai trò}
> Ngày: {YYYY-MM-DD}
> Từ: {Sale name} — Phòng Kinh doanh CES Global

## 1. Tóm tắt 30 giây
{1 đoạn 4-5 câu: hiểu pain của KH + đề xuất gì + ROI dự kiến}

## 2. Bối cảnh KH (theo tư vấn đầu)
- Lĩnh vực: ...
- Quy mô: ...
- Pain chính: 3 bullet
- Mục tiêu sau đào tạo: ...

## 3. Đề xuất CES Global
**Khóa đề xuất:** {Tên khóa} ({số buổi} · {format})
**Lý do match:** 3 bullet kết nối pain → giải pháp khóa
**Lộ trình:** bảng buổi-nội dung-output

## 4. Hệ sinh thái CES (USP)
- LMS Academy academy.cesglobal.com.vn
- Repo công khai GitHub (link mẫu)
- Cộng đồng 1.200+ thành viên
- Hỗ trợ sau khóa 6 tháng
{Chèn 2-3 USP từ usp-vs-competitor.md}

## 5. Đội ngũ giảng dạy
{GV theo khóa: TA / Hải / Kim Anh + credentials}

## 6. Đầu tư
| Hạng mục | Chi phí |
|---|---|
| Học phí | {HOC_PHI} |
| Ưu đãi early bird (nếu áp dụng) | -{UU_DAI}% |
| Tổng sau ưu đãi | {TONG} |

**Bao gồm:**
- Tài liệu HV (PDF + slide)
- LMS Academy 6 tháng
- Repo public + cộng đồng
- Hỗ trợ sau khóa

**Không bao gồm:** {tool 3rd party — ChatGPT Plus, Claude Pro nếu cần}

## 7. Cam kết đầu ra
- HV cuối khóa: {3-5 bullet measurable outcome}
- Nếu không đạt: {chính sách hỗ trợ thêm — buổi bổ sung free}

## 8. Bước tiếp theo
- [ ] Anh/chị xác nhận khóa + lịch khai giảng phù hợp
- [ ] Em gửi hợp đồng + lịch chi tiết
- [ ] Thanh toán đợt 1 → bắt đầu khóa

**Liên hệ:**
{Sale name} — {SĐT} — {Email}
CES Global · 222 Nguyễn Văn Tuyết, Đống Đa, HN
www.cesglobal.com.vn · cesglobal.ai@gmail.com

> *"Đồng hành chuyển đổi AI cùng doanh nghiệp."*
```

## Bước 4 — Lưu file

Default lưu vào: `outputs/proposal-{YYMMDD}-{kh-slug}.md`

Hoặc user chỉ định path khác.

## Tone check trước khi trả

- ✅ Xưng "anh/chị" + "em/mình", không "quý khách"
- ✅ Có số liệu cụ thể, không chung chung
- ✅ 4 trụ tính cách CES có trong proposal
- ✅ Placeholder `{HOC_PHI}` `{UU_DAI}` Sale fill được
- ❌ Không hạ thấp đối thủ
- ❌ Không "đảm bảo 100% thành công"

## Anti-patterns

| ❌ Sai | ✅ Đúng |
|---|---|
| "Quý công ty kính mến" | "Chào anh/chị..." |
| "Cam kết thành công 100%" | "Cam kết HV cuối khóa build được 3 use case thực" |
| Khóa generic, không tailor | Match persona + pain cụ thể từ tư vấn |
| Học phí cứng | Placeholder `{HOC_PHI}` để Sale fill |
