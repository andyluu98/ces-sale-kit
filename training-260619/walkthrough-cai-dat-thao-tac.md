# Walkthrough cài đặt + thao tác — Buổi training Sale 19/06

> Tài liệu Sale **MỞ TRÊN MÁY** trong buổi training. Mỗi bước có lệnh copy-paste + screenshot mong đợi. In ra 1 bản phụ cầm theo.

**Repo:** https://github.com/andyluu98/ces-sale-kit

---

## ⏱️ Trước buổi (Sale làm trước 8h30)

### Yêu cầu máy

- ✅ Windows 10/11 hoặc Mac
- ✅ Tài khoản Claude **Pro** (`claude.ai/upgrade` — 20$/tháng) hoặc Max
- ✅ Cài Git (`git-scm.com` → next-next-finish)
- ✅ Có tài khoản GitHub (free là đủ)

### Nếu chưa có Claude Pro

→ Hỏi A. Linh xin tài khoản team (CES có account chung) hoặc nâng cấp Pro cá nhân.

---

## 📚 8h30–08h35 · Phần 1 — Mở đầu (5')

TA dạy. **Sale chưa cần thao tác.**

Chỉ cần: mở laptop, chuẩn bị terminal sẵn.

---

## 💻 08h35–08h50 · Phần 2 — Claude basic cho Sale (15')

### Thao tác 1 — Mở Claude.ai

1. Mở browser → `claude.ai`
2. Login bằng email (Pro/Max)

**Mong đợi:** Thấy giao diện chat Claude.

### Thao tác 2 — Tạo Project đầu tiên

1. Cột trái → click **+ New Project**
2. Tên project: `KH thử nghiệm — Training 19-06`
3. Description: `Project test trong buổi training Sale`
4. Bấm **Create**

**Mong đợi:** Tạo xong project rỗng.

### Thao tác 3 — Tạo Custom Style "CES Tone"

1. Trong project → click **Set custom style**
2. Paste vào ô:

```
Tone CES Global:
- 4 trụ tính cách: chuyên nghiệp · tiên phong · thực chiến · nhân văn
- Xưng "anh/chị" + "em/mình", không "quý khách"
- Có số liệu cụ thể, không chung chung
- Không hạ thấp đối thủ
- Không "đảm bảo thành công 100%"
- Câu mở đầu là hook (số liệu/câu hỏi/tình huống thực)
- Mỗi đoạn ngắn 1-3 câu, dễ đọc
```

3. Lưu style → đặt tên: `CES Tone`

**Mong đợi:** Style xuất hiện trong danh sách.

### Thao tác 4 — Test 1 prompt cơ bản

Trong project, gõ:

```
Viết email cold gửi 1 founder startup EdTech, 
đã dùng Claude rồi, tone CES Tone.
Subject ngắn + body < 100 từ + CTA đặt 15' call.
```

**Mong đợi:** Claude ra email tone CES — xưng anh/chị, không quý khách.

---

## 🚀 08h50–09h10 · Phần 3 — Claude Code + Cowork (20')

### Thao tác 5 — Cài Claude Code

**Windows (PowerShell — bấm Win+X → chọn PowerShell):**

```powershell
iwr -useb https://claude.ai/install.ps1 | iex
```

**Mac (Terminal):**

```bash
curl -fsSL https://claude.ai/install.sh | sh
```

→ Đợi 1-2 phút cài xong.

**Test cài thành công:**

```powershell
claude --version
```

**Mong đợi:** In ra phiên bản (vd `claude version X.Y.Z`).

### Thao tác 6 — Login Claude Code

```powershell
claude
```

→ Lần đầu sẽ yêu cầu login → bấm `1` chọn "Claude account" → mở browser → login → quay lại terminal.

**Mong đợi:** Thấy prompt `>` chờ nhập lệnh.

### Thao tác 7 — Test prompt cơ bản trong Claude Code

Gõ trong Claude Code:

```
Viết 1 đoạn hello world chuẩn brand CES Global.
```

**Mong đợi:** Output đoạn ngắn chuẩn tone CES.

Gõ `/exit` để thoát.

---

## ⭐ 09h10–09h35 · Phần 4 — Clone repo + test Skill (25')

### Thao tác 8 — Clone repo ces-sale-kit

Mở terminal mới (PowerShell trên Windows hoặc Terminal Mac):

```powershell
cd ~
git clone https://github.com/andyluu98/ces-sale-kit.git
cd ces-sale-kit
```

**Mong đợi:**
```
Cloning into 'ces-sale-kit'...
remote: ...
Resolving deltas: 100% (X/X), done.
```

### Thao tác 9 — Xem cấu trúc repo

```powershell
ls
```

**Mong đợi thấy:**
- `AGENTS.md` · `README.md` · `INSTALL.md`
- `.claude/` (chứa `skills/` + `agents/`)
- `knowledge/` · `templates/` · `training-260619/`

### Thao tác 10 — Mở Claude Code trong repo

```powershell
claude
```

**Mong đợi:** Claude Code khởi động, đã ở folder `ces-sale-kit`.

### Thao tác 11 — Kiểm tra Skill đã load

Trong Claude Code gõ:

```
/skills
```

**Mong đợi thấy 7 skill:**
- `ces-sale-proposal`
- `ces-sale-quote`
- `ces-sale-script`
- `ces-sale-email`
- `ces-sale-objection`
- `ces-sale-survey`
- `ces-sale-contract`

Nếu KHÔNG thấy → check lại đang ở đúng folder `ces-sale-kit` không (`pwd` để xem).

### Thao tác 12 — Test Skill `ces-sale-script` (kịch bản)

Gõ trong Claude Code:

```
/ces-sale-script
```

Skill sẽ hỏi 6 câu — Sale trả lời theo case này:

```
1. KH: Nguyễn Văn A
2. Persona: 5 (1 person company)
3. Loại buổi: warm follow-up
4. Mục tiêu: đặt demo
5. Thời lượng: 30 phút
6. KH biết CES rồi qua đâu: đã đăng ký workshop
```

**Mong đợi:** Skill output kịch bản 5 phần đầy đủ ngay trong terminal.

### Thao tác 13 — Test Skill `ces-sale-objection`

```
/ces-sale-objection
```

Trả lời:

```
1. Objection: "Bên nào cũng dạy Claude, sao phải học CES?"
2. Context: warm follow-up
3. Persona: 5
4. Tone: lịch sự nhẹ
```

**Mong đợi:** Output script trả lời + evidence.

### Thao tác 14 — Test Skill `ces-sale-proposal`

```
/ces-sale-proposal
```

Trả lời:

```
1. KH: Nguyễn Văn A — startup EdTech
2. Persona: 1 (Founder Startup)
3. Loại: khóa public
4. Pain: dạy AI cho team 8 người
5. Quy mô: 8 người
6. Ngân sách: 50-200tr
```

**Mong đợi:** Output proposal 8 phần đầy đủ với placeholder `{HOC_PHI}`.

---

## 🤖 09h35–09h50 · Phần 5 — Agent Team (15')

### Thao tác 15 — Spawn Agent Team với 1 prompt

Trong Claude Code (vẫn ở folder `ces-sale-kit`), gõ NGUYÊN VĂN (không gõ `/`):

```
Case mới: KH = Nguyễn Văn A, founder startup EdTech 8 người,
đã dùng Claude.ai 6 tháng, hỏi "sao phải học CES".
Ngân sách <20tr. Sáng mai 10h gọi follow-up.

Tạo Agent Team xử lý case này, em cần đủ tài liệu trước 9h sáng mai.
```

**Claude Code sẽ:**
1. Đọc prompt → parse info
2. Spawn 4 Agent song song:
   - Discovery (~2')
   - Content (~3')
   - Pitch (~3')
   - Closing (~2')
3. Mỗi Agent ghi file vào `outputs/nguyen-van-a/`

**Mong đợi:** Thấy log dạng:
```
🤖 Discovery Agent đang chạy...
✅ outputs/nguyen-van-a/01-discovery.md
🤖 Content Agent đang chạy...
✅ outputs/nguyen-van-a/02-proposal.md
...
```

### Thao tác 16 — Mở folder output xem

Mở terminal khác hoặc File Explorer:

```powershell
cd outputs/nguyen-van-a
ls
```

**Mong đợi thấy 8 file:**
- `01-discovery.md` (Discovery Agent)
- `02-proposal.md` · `03-quote.md` · `04-email.md` (Content Agent)
- `05-script.md` · `06-objections.md` (Pitch Agent)
- `07-followup-timeline.md` · `08a-contract-draft.md` · `08b-email-closing.md` (Closing Agent)

Mở thử `02-proposal.md` xem nội dung.

---

## 🎬 09h50–10h00 · Phần 6 — Case Đại role-play + Q&A (10')

### Thao tác 17 — Role-play với case Đại thật

Đại nhập case thật đang tư vấn:

```
Case thật: KH = {tên KH Đại đang tư vấn}, 
{chức danh + DN/cá nhân},
đã dùng AI: {gì},
pain: {nguyên văn KH nói},
ngân sách: {khoảng},
mục tiêu Sale: {gặp/chốt/đặt demo}.

Tạo Agent Team xử lý.
```

→ Đại xem output → giữ lại 2-3 file dùng được ngay → review tone.

### Q&A — 5 phút cuối

Hỏi gì cũng được — TA + Hải on-call.

---

## ✅ Sau buổi (Sale làm tối nay/cuối tuần)

### Việc 1 — Sửa knowledge fit DN mình

Mở file `knowledge/portfolio-khoa-ces.md` trong VS Code/Notepad:

- Fill học phí thật vào placeholder `{HOC_PHI_OPC}` `{HOC_PHI_BOOTCAMP_TC}` ...
- Hỏi A. Hiếu MKT số chính thức

### Việc 2 — Add 5 objection mới gặp tuần này

Mở `knowledge/objection-bank.md`:

- Thêm objection số 13, 14, 15... mỗi Sale có gì share thêm
- Format giống objection 1-12 (Ý ẩn · Script · Evidence)

### Việc 3 — Push update lên GitHub

```powershell
cd ces-sale-kit
git add knowledge/
git commit -m "feat: cập nhật học phí + thêm 5 objection mới"
git push
```

→ Cả team Sale `git pull` để dùng update mới.

### Việc 4 — In cheat sheet 1 trang

Mở `training-260619/prompt-cheatsheet.md` → print → gấp bỏ túi.

---

## 🆘 Khi gặp lỗi — Top 5 trouble

| Lỗi | Cách fix |
|---|---|
| `claude: command not found` | Restart terminal · Check `$env:PATH` (Windows) hoặc `~/.zshrc` (Mac) |
| `/skills` không thấy skill nào | `pwd` xem có ở folder `ces-sale-kit` không · `cd ces-sale-kit` |
| Skill output cứng, không đúng brand | Đọc lại `knowledge/brand-ces-global.md` đã update chưa · Báo TA |
| Agent Team không spawn parallel | Restart Claude Code · Update Claude Code: `claude update` |
| Git push lỗi authentication | `gh auth login` → chọn HTTPS · Login lại |

---

## 📞 Hỗ trợ kỹ thuật

- **Tuấn Anh** (lead) — content + skill output
- **Hải** (Tech Lead) — cài đặt, lỗi terminal, MCP
- **A. Linh** (Sale lead) — STK · MST · brand info

Inbox nhóm CES Global hoặc trực tiếp.

---

## 🎯 Mục tiêu cuối buổi

Sale phải làm được:
- ✅ Cài Claude Code · clone repo · login
- ✅ Gõ `/ces-sale-script` ra kịch bản
- ✅ Gõ 1 prompt Agent Team ra 8 file
- ✅ Edit `knowledge/portfolio-khoa-ces.md` thêm khóa mới
- ✅ Push update lên GitHub cho team dùng chung

**Nếu chưa làm được → ping Hải/TA buổi chiều, làm 1-1.**
