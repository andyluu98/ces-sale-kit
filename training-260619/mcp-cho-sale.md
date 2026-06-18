# 3 MCP cài cho Sale CES Global

> Hướng dẫn cài 3 MCP server hữu ích nhất cho Sale. Cài tự chọn — bắt đầu với MCP 1 vì lợi ích rõ nhất.

## Tổng quan

| MCP | Lợi ích | Độ khó cài | Ưu tiên |
|---|---|---|---|
| **1. `obsidian-opck1`** | Đọc vault CES Brain — brand, portfolio, KH cũ, note Sếp | Dễ | ⭐⭐⭐ |
| **2. `ces-sop`** | Tra SOP nội bộ CES — quy trình tư vấn/báo giá | Dễ (đã có) | ⭐⭐ |
| **3. `Windows-MCP`** | Tự động hóa desktop — mở Excel, gửi email, screenshot | Trung | ⭐⭐ |

---

## MCP 1 — `obsidian-opck1` (Vault CES Brain)

### Lợi ích

- Tra cứu brand guideline đúng nhất (file vault > file trên Drive)
- Đọc portfolio khóa với chi tiết update mỗi tuần
- Truy cập note KH cũ — "KH X tư vấn cách đây 3 tháng nói gì?"
- Đọc note họp Sếp, decision log

### Cài (5 phút)

**Bước 1 — Mở Obsidian vault OPC-K1**

Vault path: `F:\00000. Obsidian Vault\1_OPC_K1\OPC-K1`

**Bước 2 — Cài plugin "Local REST API" trong Obsidian**

1. Mở Obsidian → Settings → Community plugins
2. Browse → search "Local REST API" → Install
3. Enable plugin
4. Settings của plugin: copy **API Key** (chuỗi dài)

**Bước 3 — Thêm vào Claude Code config**

Mở file `~/.claude/mcp.json` (tạo nếu chưa có):

```json
{
  "mcpServers": {
    "obsidian-opck1": {
      "type": "http",
      "url": "http://127.0.0.1:27123/mcp/",
      "headers": {
        "Authorization": "Bearer DÁN_API_KEY_VÀO_ĐÂY"
      }
    }
  }
}
```

**Bước 4 — Restart Claude Code → test**

```
Trong Claude Code gõ:
"Liệt kê 5 file mới nhất trong vault"

→ Claude trả về list file vault.
```

### Use case Sale hàng ngày

```
"Tìm KH cũ ngành EdTech đã tư vấn 3 tháng qua, gom thành bảng"
"Brand voice CES Global hiện tại trên vault — tóm tắt 5 điểm chính"
"Note họp với KH Hoà Phát lần cuối — em chưa đọc, tóm tắt giúp"
"Portfolio khóa CES update mới nhất — có khóa nào ra trong T7?"
```

### Lưu ý

- Obsidian PHẢI mở khi dùng MCP này (Local REST API chạy local)
- Nếu Obsidian đóng → MCP timeout → mở lại là OK
- API key bảo mật — không share công khai

---

## MCP 2 — `ces-sop` (SOP nội bộ)

### Lợi ích

- Tra SOP đã chuẩn hóa — không phải search Drive thủ công
- Quy trình tư vấn / báo giá / chốt deal đã có sẵn

### Cài

**Đã có sẵn trong CES setup.** Nếu chưa có trong `~/.claude/mcp.json`:

```json
{
  "mcpServers": {
    "ces-sop": {
      "command": "node",
      "args": ["{path-to-ces-sop-mcp-server}/index.js"]
    }
  }
}
```

→ Hỏi Hải (Tech Lead) hoặc TA đường dẫn server.

### Use case

```
"SOP báo giá in-house cho DN >500 người là gì?"
"Quy trình chốt deal khi KH yêu cầu phụ lục riêng"
"SOP gửi proposal — checklist trước khi gửi"
```

---

## MCP 3 — `Windows-MCP` (Tự động hóa desktop)

### Lợi ích

- Mở Excel/Word file proposal cũ để Sale tham khảo
- Screenshot màn hình KH gửi để gắn vào proposal
- Tự động click trong CRM (push lead)
- Mở Outlook gửi email (sau khi review)

### Cài (10 phút)

**Bước 1 — Tải Windows-MCP**

GitHub: search "Windows-MCP" → tải release Windows mới nhất → giải nén.

**Bước 2 — Cài Python (nếu chưa có)**

Tải python.org → version 3.11+.

**Bước 3 — Cài dependencies**

```powershell
cd C:\path\to\Windows-MCP
pip install -r requirements.txt
```

**Bước 4 — Thêm vào `~/.claude/mcp.json`**

```json
{
  "mcpServers": {
    "Windows-MCP": {
      "command": "python",
      "args": ["C:\\path\\to\\Windows-MCP\\server.py"]
    }
  }
}
```

**Bước 5 — Restart Claude Code → test**

```
"Screenshot màn hình hiện tại"
"Mở file Excel ProposalMau.xlsx ở Desktop"
```

### Use case Sale

```
"Mở file proposal cũ ProposalMau_TH-TrueMilk.docx
ở Drive, tóm tắt cho em xem 5 ý chính"

"Screenshot bảng giá KH gửi trên Zalo,
gắn vào proposal đang soạn"

"Mở Outlook, tạo email mới gửi {KH},
subject + body theo template em soạn"
```

### Lưu ý bảo mật

- ⚠️ MCP này điều khiển desktop — chỉ cấp quyền task cụ thể
- KHÔNG cho phép Claude tự động gửi email không review
- KHÔNG cho phép Claude truy cập file nhạy cảm (HĐ ký, MST KH)
- Sale review trước mỗi action MCP

---

## Optional — MCP khác có thể thêm

| MCP | Khi nào dùng |
|---|---|
| `chatgpt-image` | Gen ảnh banner/infographic cho proposal |
| `Figma` | Đọc mockup design brand |
| `social-content` | Đăng auto FB/IG sau khi Sale chốt content |
| `notion` | Nếu Sale dùng Notion lưu pipeline KH |
| `mcp-obsidian-saoviet` | Nếu Sale phụ trách KH Sao Việt riêng |

→ Thêm sau khi 3 MCP chính chạy ổn.

---

## Khi MCP timeout / không response

| Triệu chứng | Nguyên nhân | Cách fix |
|---|---|---|
| `obsidian-opck1` timeout | Obsidian đóng / plugin đứng | Mở lại Obsidian → restart Claude Code |
| `ces-sop` not found | Path sai | Hỏi Hải đường dẫn server |
| `Windows-MCP` báo lỗi Python | Python chưa cài | Tải python.org 3.11+ |
| Tất cả MCP đều fail | Sai format `mcp.json` | Validate JSON tại jsonlint.com |

---

## Hỗ trợ

- Cài lần đầu: Hải (Tech Lead) — request help
- Sai cấu hình: copy `~/.claude/mcp.json` paste cho Hải xem
- Tính năng mới: PR vào repo `ces-sale-kit`
