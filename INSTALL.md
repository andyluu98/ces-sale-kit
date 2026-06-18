# Cài đặt CES Sale Kit (5 phút)

> Hướng dẫn dành cho team Sale CES Global. Không cần biết code.

## Yêu cầu

- Máy tính Windows/Mac
- Tài khoản Claude (Pro hoặc Max — claude.ai)
- 30 phút (lần đầu)

---

## Bước 1 — Cài Claude Code

**Windows:**
1. Mở PowerShell
2. Chạy: `iwr -useb https://claude.ai/install.ps1 | iex`
3. Mở Claude Code: gõ `claude` trong terminal

**Mac:**
1. Mở Terminal
2. Chạy: `curl -fsSL https://claude.ai/install.sh | sh`
3. Mở Claude Code: gõ `claude`

→ Lần đầu login bằng tài khoản Claude.

---

## Bước 2 — Clone repo CES Sale Kit

```bash
cd ~
git clone https://github.com/andyluu98/ces-sale-kit.git
cd ces-sale-kit
```

→ Nếu chưa cài Git: tải tại git-scm.com → cài next-next-finish.

---

## Bước 3 — Đăng ký skills với Claude Code

Repo đã có sẵn folder `.claude/skills/` — Claude Code sẽ tự nhận khi mở terminal trong folder repo.

**Kiểm tra:**
```bash
cd ces-sale-kit
claude
```

Trong Claude Code gõ:
```
/skills
```

→ Nếu thấy 7 skill `ces-sale-*` xuất hiện → OK.

---

## Bước 4 — Cài 3 MCP (optional nhưng khuyến nghị)

Xem `training-260619/mcp-cho-sale.md` — hướng dẫn cài:
- `obsidian-opck1` — đọc vault CES Brain
- `ces-sop` — tra SOP
- `Windows-MCP` — tự động hóa desktop

---

## Bước 5 — Test thử

Trong Claude Code (đang ở folder ces-sale-kit), gõ:

```
/ces-sale-kich-ban
```

→ Claude sẽ hỏi: KH là ai? B2B/B2C? Persona? Pain point?

→ Trả lời → Skill ra kịch bản tư vấn.

---

## Troubleshoot

| Lỗi | Cách fix |
|---|---|
| `claude: command not found` | Restart terminal hoặc add Claude vào PATH |
| `/skills` không thấy skill | Check đang ở đúng folder `ces-sale-kit` không |
| Skill output không đúng brand | Update `knowledge/brand-ces-global.md` rồi gọi lại |

---

## Liên hệ hỗ trợ

- Tuấn Anh — Lead Phòng Dự Án (maintain kit)
- Hải — Tech Lead (issues kỹ thuật)

→ Inbox group team CES Global.
