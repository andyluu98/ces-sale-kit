# Walkthrough cài đặt + thao tác + PROMPT thực hành — Training Sale 19/06

> **Sale MỞ FILE NÀY TRÊN MÁY** trong buổi training. Mỗi thao tác có:
> - Lệnh/prompt **COPY-PASTE TRỰC TIẾP** (không phải sửa)
> - **Output mong đợi** mẫu để biết đúng/sai
> - 10 prompt EXTRA cuối file để Sale practice sau buổi

**Repo:** https://github.com/andyluu98/ces-sale-kit

---

## ⏱️ Trước buổi (Sale làm trước 8h30)

### Yêu cầu máy

- ✅ Windows 10/11 hoặc Mac
- ✅ Tài khoản Claude **Pro** (`claude.ai/upgrade` — 20$/tháng) hoặc Max
- ✅ Cài Git: `git-scm.com` → next-next-finish (Win) hoặc `brew install git` (Mac)
- ✅ Có tài khoản GitHub free

Chưa có Claude Pro → hỏi Linh xin tài khoản team CES.

---

## 📚 08h30–08h35 · Phần 1 — Mở đầu (5')

TA dạy. Sale chỉ cần mở laptop, terminal sẵn.

---

## 💻 08h35–08h50 · Phần 2 — Claude basic cho Sale (15')

### Thao tác 1 — Mở claude.ai + Login

1. Browser → `https://claude.ai`
2. Login bằng email Pro/Max
3. Vào giao diện chat

**Output mong đợi:** Thấy ô gõ "How can I help you today?" ở giữa màn hình.

---

### Thao tác 2 — Tạo Project "KH thử nghiệm"

1. Cột trái → click **+ New Project**
2. Name: `KH thử nghiệm — Training 19-06`
3. Description: `Project test trong buổi training Sale`
4. Click **Create**

**Output mong đợi:** Project mới hiện trong sidebar, ô chat ghi "What are you working on with [project name]?"

---

### Thao tác 3 — Tạo Custom Style "CES Tone"

1. Trong project → click avatar góc phải dưới ô gõ → **Choose style** → **Create custom style**
2. **Paste vào ô instructions:**

```
Bạn là Sale CES Global. Tone giao tiếp 4 trụ:
1. Chuyên nghiệp — có số liệu, dẫn chứng, không chung chung
2. Tiên phong — định vị AI First, không "theo trend"
3. Thực chiến — kết quả đo được, không lý thuyết
4. Nhân văn — "AI không thay thế con người, AI giúp con người làm tốt hơn"

Xưng hô: "anh/chị" (KH) + "em/mình" (Sale). KHÔNG dùng "quý khách".

Câu mở đầu phải là hook: câu hỏi · số liệu · tình huống thực.

Mỗi đoạn ngắn 1-3 câu, có xuống dòng để dễ đọc trên mobile.

TUYỆT ĐỐI TRÁNH:
- "AI sẽ thay thế con người"
- "Đảm bảo thành công 100%"
- "Quý khách hàng vui lòng..."
- Buzzword rỗng ("đột phá toàn diện cách mạng số")
- Hạ thấp đối thủ (ChatGPT, Gemini, Microsoft Copilot)

Tagline có thể dùng cuối bài:
- "Đồng hành chuyển đổi AI cùng doanh nghiệp"
- "Kinh doanh hiệu quả — Phát triển bền vững"

Sản phẩm CES: AI GATE · CES EDU AI · 9 dòng đào tạo · 100k+ KH · Top 10 thương hiệu tín nhiệm QG.
```

3. Đặt tên: `CES Tone` → **Save**

**Output mong đợi:** Style "CES Tone" xuất hiện trong dropdown chọn style.

---

### Thao tác 4 — Test prompt soạn email cold

Trong project, chọn Style "CES Tone", **paste prompt nguyên văn:**

```
Soạn email cold gửi anh Nguyễn Văn A — founder startup EdTech 8 người tại Hà Nội. 

Em đã thấy startup này huy động seed round 2 tỷ tháng trước, đang scale team. 

Mục tiêu email: đặt 1 buổi call 15 phút để pitch khóa "AI Agent cho Doanh nghiệp 6 buổi" của CES Global. 

Yêu cầu:
- Subject < 70 ký tự, có tên KH + giá trị cụ thể
- Body < 100 từ
- Hook bằng số liệu hoặc câu hỏi (không nịnh)
- Có 1 social proof (KH lớn CES đã làm)
- CTA cụ thể: "tuần này anh tiện khung nào?"
- Tone CES Tone (đã set)

Trả về format: Subject | Body | Note 1 dòng giải thích chọn hook gì.
```

**Output mong đợi (mẫu):**

```
Subject: Anh A — 6 buổi AI cho team startup EdTech 8 người

Body:
Em là [Tên] từ CES Global. Em vừa thấy [Tên DN] huy động seed 2 tỷ — chúc mừng anh!

8 người scale nhanh thường gặp 1 pain: team chưa kịp dùng AI để leverage. CES vừa làm in-house cho VNPT — sau 6 buổi, đội 12 người tiết kiệm 8h/tuần.

Em xin 15' call tuần này để xem có giúp được [Tên DN] không. Anh tiện thứ mấy ạ?

Em cảm ơn anh.

---
Note: Hook bằng tin huy động + số liệu cụ thể (8h/tuần) thay vì nịnh chung chung.
```

→ Test 2-3 prompt khác với case khác nhau để quen.

---

## 🚀 08h50–09h10 · Phần 3 — Claude Code + Cowork (20')

### Thao tác 5 — Cài Claude Code

**Windows (PowerShell):**

```powershell
iwr -useb https://claude.ai/install.ps1 | iex
```

**Mac (Terminal):**

```bash
curl -fsSL https://claude.ai/install.sh | sh
```

Đợi 1-2 phút.

**Test cài OK:**

```powershell
claude --version
```

**Output mong đợi:**
```
claude version 1.x.x
```

---

### Thao tác 6 — Login Claude Code

```powershell
claude
```

Lần đầu yêu cầu login:
1. Chọn `1` cho "Claude account"
2. Browser tự mở → login
3. Quay lại terminal

**Output mong đợi:**
```
✓ Logged in as [your-email]
> 
```

(Dấu `>` là prompt chờ nhập)

---

### Thao tác 7 — Test prompt cơ bản trong Claude Code

**Paste prompt nguyên văn vào Claude Code:**

```
Giới thiệu CES Global trong 50 từ, tone chuyên nghiệp nhưng thân thiện. 
Nhấn 3 ý: AI First · 10+ năm · 100k+ KH (Hoà Phát, VNPT, Bảo Việt). 
Kết bằng tagline "Đồng hành chuyển đổi AI cùng doanh nghiệp".
```

**Output mong đợi:**
```
CES Global là DN AI First tiên phong tại Việt Nam — 10+ năm đào tạo và 
triển khai AI cho hơn 100.000 khách hàng, trong đó có Hoà Phát, VNPT, 
Bảo Việt. Chúng em không bán "khóa học", em bán lộ trình + cộng đồng + 
hỗ trợ 6 tháng sau đào tạo.

"Đồng hành chuyển đổi AI cùng doanh nghiệp."
```

Gõ `/exit` thoát Claude Code.

---

## ⭐ 09h10–09h35 · Phần 4 — Clone repo + Test 3 Skill (25')

### Thao tác 8 — Clone repo ces-sale-kit

Trong terminal mới:

```powershell
cd ~
git clone https://github.com/andyluu98/ces-sale-kit.git
cd ces-sale-kit
```

**Output mong đợi:**
```
Cloning into 'ces-sale-kit'...
remote: Enumerating objects: 30, done.
remote: Counting objects: 100% (30/30), done.
remote: Compressing objects: 100% (28/28), done.
Receiving objects: 100% (30/30)...
Resolving deltas: 100% (X/X), done.
```

---

### Thao tác 9 — Mở Claude Code trong repo

```powershell
claude
```

**Output mong đợi:** Claude Code load, hiển thị folder đang ở.

---

### Thao tác 10 — Kiểm tra 7 Skill đã load

**Gõ trong Claude Code:**

```
/skills
```

**Output mong đợi (thấy 7 skill):**
```
Available skills:
- ces-sale-de-xuat — Soạn proposal CES Global...
- ces-sale-bao-gia — Soạn bảng báo giá CES Global...
- ces-sale-kich-ban — Gen kịch bản tư vấn Sale...
- ces-sale-email — Soạn email Sale CES Global...
- ces-sale-xu-ly-tu-choi — Xử lý objection KH...
- ces-sale-khao-sat — Soạn form khảo sát KH...
- ces-sale-hop-dong — Soạn hợp đồng đào tạo...
```

KHÔNG thấy → `pwd` check folder · `cd ces-sale-kit` nếu sai.

---

### Thao tác 11 — Test Skill `ces-sale-kich-ban` (kịch bản tư vấn)

**Gõ prompt nguyên văn (KHÔNG dùng /command, dùng câu tự nhiên gọi skill):**

```
Dùng skill ces-sale-kich-ban để soạn kịch bản gọi cold 10 phút cho case sau:

KH: anh Nguyễn Văn A
Chức danh: Founder
DN: startup EdTech 8 người, ở Hà Nội
Persona: P1 — Founder Startup
Đã dùng AI: ChatGPT 6 tháng, đang nghĩ nâng cấp Claude
Pain quan sát: team chưa biết dùng AI để scale content marketing
Mục tiêu buổi gọi: đặt lịch gặp 30 phút tuần này

Yêu cầu:
- Kịch bản 5 phần (mở · discovery · pitch · objection · closing)
- Bao gồm 5 câu discovery cụ thể
- Top 3 objection có thể gặp + script trả lời mỗi cái
- Tone CES — đồng nghiệp ngang hàng, không thấp giọng xin việc
- Quy tắc 70/30 (KH 70%, Sale 30%)
```

**Output mong đợi (snippet):**

```markdown
# KỊCH BẢN GỌI COLD 10' — Anh Nguyễn Văn A

## Phần 1 — Mở đầu (1')
"Em chào anh A. Em là [Tên] từ CES Global. Em thấy [Tên DN] đang scale 
team 8 người sau seed round — em xin 2 phút thôi, anh có tiện không?"

→ Mục tiêu: lấy 2 phút lắng nghe, KHÔNG pitch.

## Phần 2 — Discovery (4-5')
1. [Warm-up] "Anh làm Founder bao lâu rồi ạ? Đội ngũ 8 người gồm 
   những vai trò gì?"
   *Vì sao hỏi: hiểu cơ cấu team để pitch khóa đúng phòng ban.*

2. [Quy trình] "Một tuần điển hình team marketing tốn bao nhiêu 
   giờ làm content?"
   *Vì sao hỏi: lấy số liệu cụ thể để pitch ROI sau.*

[... 3 câu nữa]

## Phần 3 — Pitch (2')
"Em hiểu — vấn đề lớn nhất là team chưa scale được content. Khóa AI 
Agent DN 6 buổi của CES vừa làm cho VNPT — sau khóa, team marketing 
của họ ra 5 bài/ngày thay vì 1 bài/2 ngày..."

## Phần 4 — Top 3 Objection
1. "Bên nào cũng dạy Claude" → [script trả lời]
2. "Giá cao" → [script]
3. "Tôi tự học YouTube được" → [script]

## Phần 5 — Closing (1-2')
[3 lựa chọn: mạnh/TB/nhẹ]
```

---

### Thao tác 12 — Test Skill `ces-sale-xu-ly-tu-choi`

**Paste prompt:**

```
Dùng skill ces-sale-xu-ly-tu-choi. Case:

KH = anh Nguyễn Văn A, persona P5 (1 person company - freelancer marketing).
KH nói nguyên văn: "Em đã dùng Claude.ai 6 tháng rồi, sao phải mất tiền học CES?"
Context: warm follow-up sau khi KH đăng ký workshop.
Tone KH: lịch sự nhẹ, không gay gắt.

Yêu cầu output:
- Phân tích ý ẩn của KH
- Script trả lời 3-5 câu (đọc lên dùng được)
- 3 evidence cụ thể kèm (case study · repo · số liệu)
- Bước tiếp theo nếu KH OK
- Bước tiếp theo nếu KH vẫn từ chối (KHÔNG push lần 3)
```

**Output mong đợi (snippet):**

```markdown
## Phân tích
- **Ý ẩn:** KH thấy AI tool là commodity, không hiểu giá trị "lộ trình + 
  cộng đồng". Đã thử Claude → tự tin tự học được.
- **Persona context:** P5 hay gặp objection này (case Đại Sale)
- **Tone match:** nhẹ — KH lịch sự, không cần phản công mạnh

## Script trả lời
"Anh A nói đúng — tool ai cũng có. Nhưng dùng tool ≠ build Agent ≠ deploy 
cho công việc lặp. Em giải thích nhanh:

Anh đã dùng Claude 6 tháng — anh đã build được AI Agent đầu tiên giúp anh 
giảm 5h/tuần chưa ạ? Nếu chưa, vấn đề không phải tool, mà là LỘ TRÌNH.

CES không bán Claude — em bán lộ trình + repo mẫu + cộng đồng 1200 người 
để anh không phải tự bơi. Anh thử mở repo này 5 phút: 
github.com/andyluu98/ces-marketing-agent-kit — đó là output HV Workshop 
Marketing tuần trước. Nếu thấy anh tự làm được trong 6 tháng tới, em không 
pitch tiếp."

## Evidence
1. Repo: github.com/andyluu98/ces-marketing-agent-kit (mở 5 phút)
2. Case Đại đã ghi lại: HV 1 person company sau khóa OPC build Agent 
   tự động hóa 70% công việc content
3. Số liệu cộng đồng: 1.200+ thành viên CES Academy

## Bước tiếp theo nếu KH OK
- Đặt lịch demo 30' tuần này để xem 1 use case cụ thể
- Gửi link repo cho anh xem trước

## Bước tiếp theo nếu KH từ chối
- KHÔNG push lần 3
- "Em hiểu — anh thử repo trước. Em set reminder Q3, lúc đó review lại."
- Gửi 1 ebook free về xu hướng AI Agent giữ kết nối
```

---

### Thao tác 13 — Test Skill `ces-sale-de-xuat`

**Paste prompt:**

```
Dùng skill ces-sale-de-xuat. Case:

KH: Công ty EdTech ABC (anh Nguyễn Văn A là Founder)
Persona: P1 — Founder Startup
Ngành: EdTech, vừa huy động seed 2 tỷ
Quy mô: 8 người (1 founder + 4 dev + 2 marketing + 1 sale)
Pain top 3:
  1. Team marketing chậm, content ra 1 bài/2 ngày
  2. Dev cũng muốn dùng AI nhưng setup mỗi người mỗi kiểu
  3. Founder muốn cả công ty AI-First trong 6 tháng

Khóa đề xuất: AI Agent cho Doanh nghiệp — 6 buổi · 2.5h/buổi · 
hybrid (3 online + 3 offline tại HN)

Ngân sách KH chia sẻ: 50-200tr cho training năm này

Yêu cầu output:
- Proposal đầy đủ 8 phần theo template
- Tóm tắt 30 giây hấp dẫn ở đầu
- Lộ trình 6 buổi chi tiết (mỗi buổi 1 dòng output HV)
- ROI dự kiến quy ra giờ tiết kiệm + tiền
- Placeholder {HOC_PHI} {UU_DAI} để Sale fill sau
- File lưu vào outputs/edtech-abc/02-proposal.md
```

**Output mong đợi:**

Skill gen file `outputs/edtech-abc/02-proposal.md` đầy đủ 8 phần. Trong terminal hiển thị tóm tắt + path file.

**Mở file kiểm tra:**

```powershell
# Trong terminal khác:
cat outputs/edtech-abc/02-proposal.md
# Hoặc mở bằng VS Code:
code outputs/edtech-abc/02-proposal.md
```

---

## 🤖 09h35–09h50 · Phần 5 — Agent Team (15')

### Thao tác 14 — Spawn Agent Team với 1 prompt

**Paste prompt NGUYÊN VĂN vào Claude Code:**

```
Case mới: Anh Nguyễn Văn A — founder startup EdTech ABC tại Hà Nội. 
Quy mô 8 người (1 founder + 4 dev + 2 marketing + 1 sale). 
Vừa huy động seed 2 tỷ tháng trước.

Đã dùng AI: ChatGPT Plus 6 tháng. Đang cân nhắc nâng Claude Pro.

Pain chính KH chia sẻ:
1. Team marketing chậm — content ra 1 bài/2 ngày
2. Dev mỗi người dùng AI mỗi kiểu, không có workflow chung  
3. Founder muốn cả công ty AI-First trong 6 tháng

KH nói nguyên văn: "Bên nào cũng dạy Claude rồi, sao phải học CES?"

Ngân sách: 50-200tr/năm cho training.

Sáng mai 10h em gọi follow-up. Em cần đủ tài liệu trước 9h sáng mai.

Tạo Agent Team xử lý case này. Slug folder output: edtech-abc.
```

**Output mong đợi (Claude Code log):**

```
Em hiểu — đây là case end-to-end. Em sẽ spawn 4 Agent song song:

🤖 Discovery Agent đang chạy...
   Đọc info KH · Phân tích pain · Match persona · Gen 5 câu discovery
   ✅ outputs/edtech-abc/01-discovery.md (Persona P1 confirmed, 7 pain)

🤖 Content Agent đang chạy...
   Đọc Discovery · Chọn khóa fit · Gen proposal + báo giá + email
   ✅ outputs/edtech-abc/02-proposal.md
   ✅ outputs/edtech-abc/03-quote.md
   ✅ outputs/edtech-abc/04-email.md

🤖 Pitch Agent đang chạy...
   Soạn kịch bản gọi 30' · 7 objection custom
   ✅ outputs/edtech-abc/05-script.md
   ✅ outputs/edtech-abc/06-objections.md

🤖 Closing Agent đang chạy...
   Timeline follow-up · HĐ draft · email closing
   ✅ outputs/edtech-abc/07-followup-timeline.md
   ✅ outputs/edtech-abc/08a-contract-draft.md
   ✅ outputs/edtech-abc/08b-email-closing.md

⏱️ Hoàn thành 8 file trong 7 phút 23 giây.

📌 Lưu ý Sale:
- Fill {HOC_PHI} sau khi xác nhận khóa (AI Agent DN 6 buổi)
- Verify ngân sách 50-200tr — em đề xuất gói 90tr (đã ưu đãi 10% early bird)
- HĐ draft cần gửi pháp chế A. Tiệp + Linh trước khi ký
- Top objection để chuẩn bị: "Bên nào cũng dạy Claude" — script ở file 06
```

---

### Thao tác 15 — Mở folder output xem 8 file

**Terminal khác hoặc File Explorer:**

```powershell
cd outputs/edtech-abc
ls
```

**Output mong đợi:**
```
01-discovery.md
02-proposal.md
03-quote.md
04-email.md
05-script.md
06-objections.md
07-followup-timeline.md
08a-contract-draft.md
08b-email-closing.md
```

**Mở từng file kiểm tra:**

```powershell
code .   # mở cả folder trong VS Code
# Hoặc đọc trong terminal:
cat 01-discovery.md
cat 02-proposal.md
```

---

## 🎬 09h50–10h00 · Phần 6 — Case Đại role-play + Q&A (10')

### Thao tác 16 — Đại role-play với case THẬT

**Đại paste case thật đang tư vấn (thay info vào template):**

```
Case thật: KH = [TÊN KH THẬT], 
[Chức danh + DN/cá nhân], 
[Ngành/lĩnh vực],
quy mô [N người],
đã dùng AI: [ChatGPT/Claude/Gemini/chưa],
pain nguyên văn KH nói: "[paste nguyên văn]",
ngân sách: [khoảng tiền hoặc "chưa rõ"],
mục tiêu Sale: [gặp/chốt/đặt demo],
[Thời điểm gọi tiếp theo].

Tạo Agent Team xử lý. Slug folder: [tên-kh-slug].
```

**Đại xem 8 file output → giữ 2-3 file dùng được ngay → review tone.**

### Q&A 5 phút cuối

TA + Hải on-call. Top câu dự đoán:
- "Em không biết code, có dùng được Skill không?" → Có, Skill che hết phần code
- "Output gen ra gửi thẳng KH được không?" → Cần review + fill placeholder học phí
- "Agent Team có thay GV không?" → Không, là công cụ, GV vẫn cần
- "Lỡ Skill output sai thì sao?" → Refine 3 vòng (xem cheatsheet)

---

## 📦 BONUS — 10 PROMPT EXTRA cho Sale practice SAU BUỔI

> Mỗi prompt copy-paste vào Claude Code (trong folder ces-sale-kit). Practice 1 prompt/ngày trong tuần.

### Prompt 1 — Soạn báo giá in-house cho DN lớn

```
Dùng skill ces-sale-bao-gia. Case:

KH: Công ty Bảo Việt — Phòng Đào tạo & Phát triển nhân sự
Khóa: In-house "AI cho Nhân sự" — 4 buổi · 3h/buổi · offline tại Bảo Việt
Số HV: 25 người
Ưu đãi: 10% (KH lớn lâu năm)
Thanh toán: 2 đợt 50-50, đợt 1 trong 7 ngày sau ký HĐ

Yêu cầu: Bảng báo giá đầy đủ + STK + thông tin xuất hóa đơn + 
điều kiện thanh toán + cam kết đầu ra.
```

### Prompt 2 — Soạn email closing chốt deal

```
Dùng skill ces-sale-email. Case:

KH: chị Nguyễn Thị B — HRM tại Công ty Nhựa Tiền Phong
Đã OK proposal khóa AI cho Nhân sự, giá 65tr
Cần: email kèm hợp đồng + STK + bước tiếp theo

Yêu cầu:
- Type 7 (Closing)
- Subject ngắn rõ
- Body < 150 từ
- Có STK đầy đủ
- 3 bước rõ ràng sau khi KH ký
```

### Prompt 3 — Xử lý objection "Tôi đang dùng FUNiX/Topica rồi"

```
Dùng skill ces-sale-xu-ly-tu-choi. Case:

KH = chị Trần Thị C — Giám đốc một trường mầm non quốc tế
Persona: P3 (HRM/L&D Manager — adapted cho giáo dục)
Objection nguyên văn: "Bên em đang đào tạo nhân viên qua FUNiX, 
khóa rất rẻ và đa dạng. Sao phải đổi sang CES?"
Tone: nhẹ nhưng có chút phòng thủ

Yêu cầu:
- KHÔNG hạ thấp FUNiX
- Chỉ ra khác biệt: FUNiX = trường tổng quát, CES = AI-First specialist
- Đưa evidence cụ thể
- Đề xuất "thử khóa 1 buổi pilot" thay vì pitch full course ngay
```

### Prompt 4 — Soạn form khảo sát pre-in-house B2B

```
Dùng skill ces-sale-khao-sat. Case:

KH: Tập đoàn Hàng Hải — Phòng Đào tạo nhân sự
Mục đích: Khảo sát nhu cầu đào tạo AI trước khi tailor curriculum in-house
Đối tượng khảo sát: 5 trưởng phòng + 1 PGĐ phụ trách HR
Format: Google Form

Yêu cầu:
- Type 5 (Pre-in-house B2B)
- 15-18 câu chia 5 section
- Có ngân sách + timeline ra quyết định
- Confirmation message ấm áp
- KÈM CẢ Google Apps Script tự sinh Form từ markdown này
```

### Prompt 5 — Spawn Agent Team cho KH cũ tái ký

```
Case tái ký: KH = anh Lê Minh D — CTO startup Fintech XYZ
KH cũ đã học Codex Workshop 3 tháng trước, đánh giá 9/10
Giờ muốn đào tạo TOÀN BỘ team dev 12 người
Pain mới: dev junior chưa quen Claude Code workflow
Ngân sách: 200-400tr
Cần proposal mới + lịch in-house

Tạo Agent Team xử lý. Slug folder: fintech-xyz-tai-ky.
```

### Prompt 6 — Soạn kịch bản gặp face-to-face 60 phút

```
Dùng skill ces-sale-kich-ban. Case:

KH: anh Phạm Văn E — Tổng Giám đốc một DN sản xuất thực phẩm 200 người
Persona: P1 + P3 hybrid (Founder + HRM concerns)
Đã gặp 1 lần — quan tâm khóa in-house, nhưng còn đang so 3 vendor

Loại buổi: face-to-face 60 phút tại văn phòng KH
Mục tiêu: pitch khóa AI cho Sản xuất + chốt proposal
Thời lượng cụ thể: discovery 20' + pitch 20' + Q&A 15' + closing 5'

Yêu cầu:
- Quy tắc 70/30
- 10 câu discovery (chia 4 nhóm)
- 3 USP key + 1 case study tương tự (DN sản xuất)
- 5 objection chuẩn bị + script
- Closing có 3 lựa chọn theo signal KH
```

### Prompt 7 — Phân tích response Google Form Workshop

```
Em vừa thu xong response Workshop AI cho HR (24 lead).
File CSV em paste ở dưới — phân tích giúp em:

[paste CSV response Google Form vào đây]

Yêu cầu:
- Top 3 pain phổ biến nhất
- 5 lead nóng nhất (criteria: pain rõ + ngân sách >50tr + decision trong 1 tháng)
- Script gọi follow-up riêng cho mỗi lead trong top 5
- Đề xuất 1 khóa upsell phù hợp cho từng lead
```

### Prompt 8 — Soạn proposal cho khách custom — Quỹ từ thiện

```
Dùng skill ces-sale-de-xuat. Case đặc biệt:

KH: Quỹ từ thiện Thiện Tâm
Đối tượng: ~20 nhân sự — staff + tình nguyện viên
Pain: dùng AI để sắp xếp công việc tổ chức từ thiện hiệu quả hơn
  - Lên kế hoạch chiến dịch quyên góp
  - Viết content truyền thông cảm xúc
  - Sàng lọc case khẩn cấp
  - Quản lý tình nguyện viên
Đặc thù: tổ chức phi lợi nhuận, ngân sách hạn chế

Khóa đề xuất: 4 buổi custom, 2 phương án Online + Offline
Công cụ đào tạo: ChatGPT + Gemini + Claude

Yêu cầu:
- 2 phương án (Online + Offline) kèm chi phí
- Tone đặc biệt: nhân văn nhấn mạnh (phù hợp tổ chức từ thiện)
- ROI quy ra "thêm bao nhiêu KH cần giúp được tiếp cận"
- Form tham chiếu: khóa SOLO
- Output 2 file: proposal-online.md + proposal-offline.md
```

### Prompt 9 — Email nurture cho KH chưa sẵn sàng

```
Dùng skill ces-sale-email. Case:

KH: anh Vũ Văn F — CEO một chuỗi cafe 5 chi nhánh
Đã pitch 3 tuần trước, KH nói "chưa cần training AI, để Q sau"
Giờ là tháng 6, Q3 mới bắt đầu tháng 7

Yêu cầu:
- Type 8 (Nurture)
- KHÔNG pitch khóa
- Gửi 1 value miễn phí: ebook "10 cách AI tiết kiệm 5h/tuần cho chủ chuỗi F&B"
- Tone ấm áp, không guilt-trip
- Mở đầu KHÔNG nhắc "anh đã nói chưa cần"
- Để mở để KH tự rep nếu muốn
- < 80 từ body
```

### Prompt 10 — Hợp đồng in-house DN lớn với ưu đãi

```
Dùng skill ces-sale-hop-dong. Case:

Bên A: Tập đoàn Hoà Phát — Khối Đào tạo & Phát triển
Bên B: CES Global

Khóa: In-house "AI cho Lãnh đạo & Quản lý" 
- 5 buổi · 3h/buổi
- 30 lãnh đạo cấp trung
- Offline tại trụ sở Hoà Phát (Hà Nội)
- Khai giảng: 15/07/2026

Giá: 250tr (đã ưu đãi 15% KH lớn lâu năm) — đã VAT
Thanh toán: 3 đợt 40-30-30
  - Đợt 1: ngay khi ký
  - Đợt 2: trước KG 7 ngày
  - Đợt 3: sau buổi 3

Yêu cầu:
- Hợp đồng dịch vụ đào tạo (Type 2)
- 8 điều đầy đủ
- Cam kết đầu ra cụ thể (3-5 use case mỗi HV)
- Buổi bổ sung miễn phí nếu <80% đạt
- Bảo mật 3 năm
- CẢNH BÁO bắt buộc gửi pháp chế review trước ký
- Placeholder MST + STK + đại diện ký
```

---

## ✅ Sau buổi — 4 việc Sale tự làm (tối nay/cuối tuần)

### Việc 1 — Practice 10 prompt extra ở trên

Mỗi ngày 1 prompt → 1 tuần hết. So output với case thật mình đang xử lý.

### Việc 2 — Fill học phí thật vào knowledge

Mở `knowledge/portfolio-khoa-ces.md`:

- Tìm tất cả `{HOC_PHI_*}` 
- Hỏi A. Hiếu MKT số chính thức
- Replace placeholder bằng số thật
- Save file

### Việc 3 — Thêm 5 objection mới gặp tuần này

Mở `knowledge/objection-bank.md`:

- Thêm objection số 13, 14, 15... mỗi Sale có gì share thêm
- Format giống objection 1-12 (Ý ẩn · Script · Evidence)

### Việc 4 — Push update lên GitHub

```powershell
cd ~/ces-sale-kit
git add knowledge/
git commit -m "feat: cập nhật học phí + thêm 5 objection mới [tên Sale]"
git push
```

→ Cả team Sale `git pull` để dùng update mới.

---

## 🆘 Top 5 lỗi thường gặp + fix nhanh

| Lỗi | Triệu chứng | Cách fix |
|---|---|---|
| `claude: command not found` | Terminal không nhận lệnh `claude` | Restart terminal · Check `$env:PATH` (Win) hoặc `~/.zshrc` (Mac) |
| `/skills` không thấy skill | Skill list rỗng | `pwd` xem có ở folder `ces-sale-kit` · `cd ces-sale-kit` |
| Skill output không đúng brand | Tone bị generic, không xưng "anh/chị" | Re-prompt: "Output chưa đúng tone CES — xưng anh/chị, không quý khách, làm lại." |
| Agent Team không spawn 4 Agent | Chỉ thấy 1 Agent chạy | `claude update` · Restart Claude Code |
| `git push` báo lỗi auth | Push fail | `gh auth login` → chọn HTTPS · Login lại |

---

## 📞 Hỗ trợ kỹ thuật

- **Tuấn Anh** (lead) — content + skill output không ưng
- **Hải** (Tech Lead) — cài đặt, lỗi terminal, Claude Code, MCP
- **Linh** (Phụ trách Sale) — STK · MST · brand info · học phí chính thức

Inbox nhóm CES Global hoặc trực tiếp.

---

## 🎯 Mục tiêu cuối buổi

Sale phải làm được:
- ✅ Cài Claude Code · login · clone repo
- ✅ Gõ prompt skill ra output (test 3 skill chính)
- ✅ Gõ 1 prompt Agent Team ra 8 file
- ✅ Edit `knowledge/portfolio-khoa-ces.md` thêm khóa mới
- ✅ Push update lên GitHub cho team dùng chung

**Nếu chưa làm được → ping Hải/TA buổi chiều, làm 1-1.**

---

**Repo:** https://github.com/andyluu98/ces-sale-kit
**File này:** `training-260619/walkthrough-cai-dat-thao-tac.md`
