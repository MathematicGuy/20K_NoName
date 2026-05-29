# 01 — Individual Problem Scan

## Scan rộng

Scan 10 problems theo nhiều lăng kính khác nhau trong lĩnh vực học tập và nghiên cứu cá nhân.

| # | Lăng kính | Problem quan sát được | Ai đang đau? | Dấu hiệu thật |
|---|---|---|---|---|
| 1 | Lặp lại | Đọc xong paper nhưng không ghi note có cấu trúc — khi cần dùng lại phải đọc lại từ đầu | Sinh viên nghiên cứu đọc nhiều paper theo roadmap | ~30–60 phút đọc lại mỗi paper khi cần trích dẫn |
| 2 | Tốn thời gian | Trước mỗi meeting với advisor phải nhớ lại và tổng hợp tiến độ từ GitHub, note, terminal rời rạc | Sinh viên nghiên cứu báo cáo định kỳ | ~30–45 phút/lần, vẫn hay thiếu sót |
| 3 | Lặp lại | Deadline nhiều môn nằm rải rác ở nhiều LMS — không có cái nhìn tổng theo tuần | Sinh viên học song song nhiều môn | 15–20 phút/tuần check thủ công, vẫn hay miss task nhỏ |
| 4 | Lặp lại | Setup môi trường Python/GCP lặp lại mỗi khi bắt đầu project hoặc VM mới | Sinh viên làm nhiều project độc lập | Mất 20–40 phút/lần setup, hay quên bước |
| 5 | Tốn thời gian | Viết phần boilerplate báo cáo môn học (intro, format, cấu trúc LaTeX) lặp lại mỗi môn | Sinh viên cuối kỳ | Mỗi báo cáo mất 1–2 giờ riêng phần format |
| 6 | AI có thể tốt hơn | Tìm lại quyết định kỹ thuật cũ (config, kiến trúc model đã chọn) sau vài sprint | Sinh viên làm dự án dài | Phải đọc lại commit history hoặc re-discuss với nhóm |
| 7 | AI có thể tốt hơn | So sánh nhiều paper cùng lúc khi viết related work | Sinh viên viết báo cáo nghiên cứu | Mở nhiều tab, so sánh thủ công, dễ bỏ sót điểm khác biệt |
| 8 | Pain từ người khác | Thành viên nhóm hỏi lại về phân công task vì không rõ scope | Nhóm project môn học | Hỏi lại 2–3 lần/sprint trong nhóm |
| 9 | Tốn thời gian | Chuẩn bị câu hỏi trước buổi seminar hoặc paper reading session | Sinh viên nghiên cứu | 20–30 phút/buổi đọc lại paper để chuẩn bị câu hỏi |
| 10 | Lặp lại | Ghi lại kết quả thực nghiệm sau mỗi lần train model | Sinh viên làm ML research | Metric chỉ tồn tại trên terminal, sau vài run không nhớ run nào tốt nhất |

---

## Top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---|---|---|---|
| 1 | Đọc & tổng hợp paper | Workflow rõ, lặp lại nhiều lần, metric thời gian cụ thể, non-AI alternative chưa đủ mạnh | "Note đủ tốt" đo thế nào |
| 2 | Update tiến độ cho advisor | Pain có thật, tổng hợp từ nhiều nguồn là bottleneck rõ, AI có thể giúp đúng chỗ | Nguồn dữ liệu (commit, note) đủ chuẩn để AI đọc không |
| 3 | Theo dõi deadline nhiều môn | Tần suất cao (hàng tuần), impact rõ (miss deadline), giải pháp Rule đơn giản và đủ mạnh | Các LMS có API/export không, hay phải nhập tay |

Vì sao không chọn các bài khác:

- **#4 Setup môi trường**: Tần suất thấp, Non-AI alternative (Makefile/script) đã đủ mạnh — không cần phân tích thêm.
- **#5 Boilerplate báo cáo**: Template LaTeX giải quyết được phần lớn — Non-AI alternative quá mạnh.
- **#10 Log kết quả thực nghiệm**: MLflow/Weights & Biases đã giải quyết hoàn toàn bài toán tracking — không cần AI.

---

## Problem Card #1 — Đọc & tổng hợp paper nghiên cứu

**Problem 1 câu:**
Mỗi lần đọc xong paper nghiên cứu, không có bước ghi note có cấu trúc — khi cần trích dẫn hoặc so sánh phải đọc lại từ đầu, tốn 30–60 phút/paper.

**Actor:**
Sinh viên nghiên cứu đọc paper theo roadmap định sẵn (multimodal, emotion recognition, hoặc tương tự).

**Thời điểm / bối cảnh:**
Ngay sau khi đọc xong mỗi paper; hoặc trước khi viết report / meeting với advisor.

**Current workflow:**

```
1. Tìm và tải paper (PDF)
2. Đọc và highlight trong PDF reader
3. (Không có bước ghi note cấu trúc)
4. Lưu file rời, không có index
5. (Sau vài tuần) Tìm lại file → đọc lại toàn bộ
```

**Bottleneck:**
Không có bước "đọc xong → note có cấu trúc tái sử dụng được". Phải đọc lại từ đầu mỗi khi cần dùng.

**Impact:**
30–60 phút/paper khi cần dùng lại; roadmap paper dài nhưng retention thấp; khó so sánh nhiều paper cùng lúc.

**Success metric:**
Trả lời được contribution / method / result / limitation / liên hệ task hiện tại trong < 5 phút mà không mở lại PDF.

**Non-AI alternative:**
Template Notion/Obsidian với 5 field bắt buộc, điền tay — đủ nếu có kỷ luật. Không cần AI nếu làm được.

**AI hypothesis:**
AI đọc PDF → draft note theo template 5 field → người dùng review/edit → lưu vào knowledge base.

**Quick gut:**
Workflow.

### Draft current workflow

```
CURRENT STATE — ~60 phút/paper (khi cần dùng lại)

[Tìm paper: 5']
→ [Đọc + highlight PDF: 40']
→ [Không ghi note có cấu trúc]
→ [Lưu file rời, không index]
         ...sau vài tuần...
→ [Tìm lại file: 5']         <-- bottleneck bắt đầu
→ [Đọc lại highlight: 30']   <-- bottleneck chính
→ [Tự nhớ lại context: 10']
```

### Draft future workflow

```
FUTURE STATE — ~55 phút lần đầu, < 5 phút lần sau

[Tìm paper: 5']
→ [Đọc PDF: 40']
→ [AI điền draft note theo template 5 field: 1']  <-- AI step
→ [Review + chỉnh note: 9']                       <-- human boundary
→ [Lưu vào knowledge base có index]
         ...khi cần dùng lại...
→ [Tra note: < 5']

Fallback: AI điền sai/thiếu → tự điền tay theo template.
```

---

## Problem Card #2 — Theo dõi deadline nhiều môn song song

**Problem 1 câu:**
Deadline nhiều môn/dự án nằm rải rác ở nhiều nguồn, không có cái nhìn tổng theo tuần — dễ miss task nhỏ dù biết deadline lớn.

**Actor:**
Sinh viên đang học nhiều môn song song, có cả deadline bài tập, milestone dự án, và lịch nghiên cứu.

**Thời điểm / bối cảnh:**
Đầu mỗi tuần khi cần lên kế hoạch; hoặc khi cần ưu tiên task trong ngày.

**Current workflow:**

```
1. Nhớ ra cần check (không có trigger cố định)
2. Mở lần lượt từng LMS / nguồn thông tin
3. Ghi nhớ hoặc note tản mạn (không có cấu trúc)
4. Làm task khi nhớ ra hoặc gần deadline
```

**Bottleneck:**
Không có bước "gom tất cả về một chỗ theo tuần" — phải check thủ công từng nguồn, không có cái nhìn tổng.

**Impact:**
15–20 phút/tuần check thủ công; tâm lý lo ngầm; nguy cơ miss task nhỏ dù biết deadline lớn.

**Success metric:**
Mỗi sáng thứ Hai có danh sách deadline tuần đầy đủ mà không cần mở nhiều tab; số lần miss deadline = 0.

**Non-AI alternative:**
Google Calendar + checklist nhập tay mỗi đầu tuần — đủ nếu có thói quen. Rule/script đã đủ mạnh ở đây.

**AI hypothesis:**
Chưa cần AI. Rule (script kéo deadline + hiển thị theo tuần) đã giải quyết được bài toán này.

**Quick gut:**
Rule.

### Draft current workflow

```
CURRENT STATE — ~15–20 phút/tuần + risk miss deadline

[Nhớ ra cần check: không có trigger cố định]
→ [Mở LMS môn 1: 3–5']
→ [Mở LMS môn 2: 3–5']       <-- lặp lại cho mỗi môn
→ [Mở LMS môn 3: 3–5']
→ [Mở LMS môn 4: 3–5']
→ [Ghi nhớ hoặc note tản mạn] <-- bottleneck: không có cấu trúc
→ [Làm khi nhớ ra]
```

### Draft future workflow

```
FUTURE STATE — ~3 phút/tuần, 0 miss deadline

[Thứ Hai sáng: trigger cố định]
→ [Script/tool kéo deadline từ các nguồn: tự động]  <-- Rule
→ [Hiển thị danh sách deadline tuần theo ngày: 1']
→ [Người dùng xác nhận + đánh dấu ưu tiên: 2']     <-- human
→ [Làm theo danh sách]

Fallback: Nguồn không kéo được → nhập tay 1 lần/tuần.
```

---

## Problem Card #3 — Viết update tiến độ nghiên cứu cho advisor

**Problem 1 câu:**
Trước mỗi meeting với advisor, phải tự nhớ lại và tổng hợp tiến độ từ nhiều nguồn rời rạc — tốn 30–45 phút và vẫn hay bị thiếu hoặc không rõ ràng.

**Actor:**
Sinh viên nghiên cứu báo cáo tiến độ định kỳ với advisor (hàng tuần hoặc trước mỗi meeting).

**Thời điểm / bối cảnh:**
Trước mỗi buổi meeting với advisor; hoặc cuối tuần khi cần gửi update qua email/chat.

**Current workflow:**

```
1. Nhớ lại đã làm gì trong tuần (không có log)
2. Mở GitHub xem commit gần nhất
3. Mở note xem paper đã đọc
4. Mở terminal/log xem kết quả thử nghiệm
5. Tổng hợp tay thành văn bản update
6. Gửi cho advisor
```

**Bottleneck:**
Bước nhớ lại + tổng hợp từ nhiều nguồn rời rạc — không có điểm tập trung, phải mở lần lượt từng nơi rồi tự diễn đạt thành narrative.

**Impact:**
30–45 phút/lần; update hay thiếu sót hoặc không rõ; advisor phải hỏi lại → mất thêm thời gian 2 chiều.

**Success metric:**
Có bản update đầy đủ gửi được trong < 10 phút; không bị advisor hỏi lại "tuần này làm gì cụ thể?" trong 4 tuần liên tiếp.

**Non-AI alternative:**
Daily log tay (ghi 3 dòng mỗi tối về việc đã làm) — giảm bottleneck nhớ lại, nhưng không giải quyết phần tổng hợp thành narrative cho advisor.

**AI hypothesis:**
AI đọc các nguồn sẵn có (commit message, note, log) → draft bản update theo cấu trúc chuẩn → người dùng review/edit → gửi.

**Quick gut:**
Workflow.

### Draft current workflow

```
CURRENT STATE — ~45 phút/lần, hay thiếu sót

[Nhớ lại đã làm gì trong tuần: 10–15']  <-- bottleneck
→ [Mở GitHub xem commit: 5']
→ [Mở note xem paper đã đọc: 5']
→ [Mở terminal/log xem kết quả: 5']
→ [Tổng hợp tay thành văn bản: 15']     <-- bottleneck
→ [Gửi cho advisor]
```

### Draft future workflow

```
FUTURE STATE — ~10 phút/lần

[Các nguồn sẵn có: GitHub commit, note, log]
→ [AI tổng hợp thành draft update: 1']  <-- AI step
→ [Review + chỉnh: 8']                  <-- human boundary
→ [Gửi cho advisor: 1']

Fallback: AI draft thiếu context → bổ sung tay rồi gửi.
```

---

*Bản nộp cá nhân — Day 02 Lab*