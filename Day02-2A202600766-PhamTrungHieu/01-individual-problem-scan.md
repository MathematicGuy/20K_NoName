# Problem Scan — Top 3 Problem Cards
*Lĩnh vực: Học tập / Nghiên cứu cá nhân*

---

## PROBLEM CARD #1 — Đọc & Tổng hợp Paper Nghiên cứu

```
| PROBLEM CARD #1                                                  |
|                                                                  |
| Problem 1 câu:  Mỗi lần đọc xong paper, insight không được      |
|                 ghi lại có cấu trúc — khi cần dùng lại phải     |
|                 đọc lại từ đầu.                                  |
|                                                                  |
| Ai đang đau?    Sinh viên / researcher đọc nhiều paper theo      |
|                 roadmap nhưng note rải rác.                      |
|                                                                  |
| Workflow hiện tại:                                               |
| 1. Tìm paper → 2. Đọc + highlight PDF → 3. (Không note)         |
| → 4. Tìm lại file → 5. Đọc lại từ đầu                          |
|                                                                  |
| Bước nghẽn nhất:  Chuyển "đọc xong" → "note tái sử dụng được"  |
|                   (~30–60 phút/paper nếu phải đọc lại)          |
|                                                                  |
| Đo thành công bằng gì?                                          |
| Trả lời được 5 câu hỏi chuẩn về paper trong < 5 phút            |
| mà không cần mở lại PDF.                                        |
| Ví dụ: 60 phút đọc lại → dưới 5 phút tra note.                 |
|                                                                  |
| Quick gut: [ ] No AI  [ ] Rule  [x] Workflow  [ ] Agent         |
|            [ ] Chưa biết                                        |
```

### Workflow Before / After

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

### Chi tiết

| Field | Nội dung |
|---|---|
| **Problem 1 câu** | Mỗi lần đọc xong paper nghiên cứu, không có bước ghi note có cấu trúc — khi cần trích dẫn hoặc so sánh phải đọc lại từ đầu, tốn 30–60 phút/paper. |
| **Actor** | Sinh viên nghiên cứu đọc paper theo roadmap định sẵn (multimodal, emotion recognition, hoặc tương tự). |
| **Thời điểm / bối cảnh** | Ngay sau khi đọc xong mỗi paper; hoặc trước khi viết report / meeting với advisor. |
| **Current workflow** | 1. Tìm và tải paper (PDF) → 2. Đọc và highlight trong PDF reader → 3. Không có bước ghi note cấu trúc → 4. Lưu file rời, không có index → 5. (Sau vài tuần) Tìm lại file → đọc lại toàn bộ |
| **Bottleneck** | Không có bước "đọc xong → note có cấu trúc tái sử dụng được". Phải đọc lại từ đầu mỗi khi cần dùng. |
| **Impact** | 30–60 phút/paper khi cần dùng lại; roadmap paper dài nhưng retention thấp; khó so sánh nhiều paper cùng lúc. |
| **Success metric** | Trả lời được contribution / method / result / limitation / liên hệ task hiện tại trong < 5 phút mà không mở lại PDF. |
| **Non-AI alternative** | Template Notion/Obsidian với 5 field bắt buộc, điền tay — đủ nếu có kỷ luật. Không cần AI nếu làm được. |
| **AI hypothesis** | AI đọc PDF → draft note theo template 5 field → người dùng review/edit → lưu vào knowledge base. |
| **Quick gut** | [x] Workflow |

---

## PROBLEM CARD #2 — Theo dõi Deadline Nhiều Môn Song Song

```
| PROBLEM CARD #2                                                  |
|                                                                  |
| Problem 1 câu:  Deadline nhiều môn/dự án nằm rải rác nhiều nơi  |
|                 — không có cái nhìn tổng theo tuần, dễ miss     |
|                 task nhỏ.                                        |
|                                                                  |
| Ai đang đau?    Sinh viên đang chạy song song nhiều môn học và   |
|                 dự án nghiên cứu.                                |
|                                                                  |
| Workflow hiện tại:                                               |
| 1. Vào từng LMS → 2. Xem deadline riêng lẻ → 3. Ghi nhớ/note   |
| → 4. Làm khi nhớ ra                                             |
|                                                                  |
| Bước nghẽn nhất:  Không có bước "gom deadline về một chỗ theo   |
|                   tuần"  (~15–20 phút/tuần check + vẫn hay miss)|
|                                                                  |
| Đo thành công bằng gì?                                          |
| Mỗi đầu tuần biết toàn bộ deadline trong 7 ngày tới mà          |
| không cần mở nhiều tab.                                         |
| Ví dụ: check 4 nguồn riêng lẻ → 1 danh sách thống nhất.        |
|                                                                  |
| Quick gut: [ ] No AI  [x] Rule  [ ] Workflow  [ ] Agent         |
|            [ ] Chưa biết                                        |
```

### Workflow Before / After

```
CURRENT STATE — ~15–20 phút/tuần + risk miss deadline

[Nhớ ra cần check: không có trigger cố định]
→ [Mở LMS môn 1: 3–5']
→ [Mở LMS môn 2: 3–5']       <-- lặp lại cho mỗi môn
→ [Mở LMS môn 3: 3–5']
→ [Mở LMS môn 4: 3–5']
→ [Ghi nhớ hoặc note tản mạn] <-- bottleneck: không có cấu trúc
→ [Làm khi nhớ ra]

FUTURE STATE — ~3 phút/tuần, 0 miss deadline

[Thứ Hai sáng: trigger cố định]
→ [Script/tool kéo deadline từ các nguồn: tự động]  <-- Rule
→ [Hiển thị danh sách deadline tuần theo ngày: 1']
→ [Người dùng xác nhận + đánh dấu ưu tiên: 2']     <-- human
→ [Làm theo danh sách]

Fallback: Nguồn không kéo được → nhập tay 1 lần/tuần.
```

### Chi tiết

| Field | Nội dung |
|---|---|
| **Problem 1 câu** | Deadline nhiều môn/dự án nằm rải rác ở nhiều nguồn, không có cái nhìn tổng theo tuần — dễ miss task nhỏ dù biết deadline lớn. |
| **Actor** | Sinh viên đang học nhiều môn song song, có cả deadline bài tập, milestone dự án, và lịch nghiên cứu. |
| **Thời điểm / bối cảnh** | Đầu mỗi tuần khi cần lên kế hoạch; hoặc khi cần ưu tiên task trong ngày. |
| **Current workflow** | 1. Nhớ ra cần check (không có trigger cố định) → 2. Mở lần lượt từng LMS / nguồn thông tin → 3. Ghi nhớ hoặc note tản mạn → 4. Làm task khi nhớ ra hoặc gần deadline |
| **Bottleneck** | Không có bước "gom tất cả về một chỗ theo tuần" — phải check thủ công từng nguồn, không có cái nhìn tổng. |
| **Impact** | 15–20 phút/tuần check thủ công; tâm lý lo ngầm; nguy cơ miss task nhỏ dù biết deadline lớn. |
| **Success metric** | Mỗi sáng thứ Hai có danh sách deadline tuần đầy đủ mà không cần mở nhiều tab; số lần miss deadline = 0. |
| **Non-AI alternative** | Google Calendar + checklist nhập tay mỗi đầu tuần — đủ nếu có thói quen. Rule/script đã đủ mạnh ở đây. |
| **AI hypothesis** | Chưa cần AI. Rule (script kéo deadline + hiển thị theo tuần) đã giải quyết được bài toán này. |
| **Quick gut** | [x] Rule |

---

## PROBLEM CARD #3 — Viết Update Tiến độ Nghiên cứu cho Advisor

```
| PROBLEM CARD #3                                                  |
|                                                                  |
| Problem 1 câu:  Trước mỗi meeting với advisor, phải tự nhớ lại  |
|                 toàn bộ việc đã làm trong tuần từ nhiều nguồn   |
|                 — tốn thời gian và hay bị thiếu sót.            |
|                                                                  |
| Ai đang đau?    Sinh viên nghiên cứu phải báo cáo tiến độ định  |
|                 kỳ với advisor.                                  |
|                                                                  |
| Workflow hiện tại:                                               |
| 1. Nhớ lại đã làm gì → 2. Mở GitHub/note/terminal               |
| → 3. Tổng hợp tay → 4. Viết update → 5. Gửi                    |
|                                                                  |
| Bước nghẽn nhất:  Nhớ lại + tổng hợp từ nhiều nguồn rời rạc    |
|                   (~30–45 phút/lần, vẫn hay thiếu)             |
|                                                                  |
| Đo thành công bằng gì?                                          |
| Có bản update đầy đủ trong < 10 phút, không bị advisor          |
| hỏi lại "tuần này làm gì cụ thể?".                             |
| Ví dụ: 45 phút tổng hợp tay → dưới 10 phút review và gửi.      |
|                                                                  |
| Quick gut: [ ] No AI  [ ] Rule  [x] Workflow  [ ] Agent         |
|            [ ] Chưa biết                                        |
```

### Workflow Before / After

```
CURRENT STATE — ~45 phút/lần, hay thiếu sót

[Nhớ lại đã làm gì trong tuần: 10–15']  <-- bottleneck
→ [Mở GitHub xem commit: 5']
→ [Mở note xem paper đã đọc: 5']
→ [Mở terminal/log xem kết quả: 5']
→ [Tổng hợp tay thành văn bản: 15']     <-- bottleneck
→ [Gửi cho advisor]

FUTURE STATE — ~10 phút/lần

[Các nguồn sẵn có: GitHub commit, note, log]
→ [AI tổng hợp thành draft update: 1']  <-- AI step
→ [Review + chỉnh: 8']                  <-- human boundary
→ [Gửi cho advisor: 1']

Fallback: AI draft thiếu context → bổ sung tay rồi gửi.
```

### Chi tiết

| Field | Nội dung |
|---|---|
| **Problem 1 câu** | Trước mỗi meeting với advisor, phải tự nhớ lại và tổng hợp tiến độ từ nhiều nguồn rời rạc — tốn 30–45 phút và vẫn hay bị thiếu hoặc không rõ ràng. |
| **Actor** | Sinh viên nghiên cứu báo cáo tiến độ định kỳ với advisor (hàng tuần hoặc trước mỗi meeting). |
| **Thời điểm / bối cảnh** | Trước mỗi buổi meeting với advisor; hoặc cuối tuần khi cần gửi update qua email/chat. |
| **Current workflow** | 1. Nhớ lại đã làm gì trong tuần (không có log) → 2. Mở GitHub xem commit gần nhất → 3. Mở note xem paper đã đọc → 4. Mở terminal/log xem kết quả thử nghiệm → 5. Tổng hợp tay thành văn bản update → 6. Gửi cho advisor |
| **Bottleneck** | Bước nhớ lại + tổng hợp từ nhiều nguồn rời rạc — không có điểm tập trung, phải mở lần lượt từng nơi rồi tự diễn đạt thành narrative. |
| **Impact** | 30–45 phút/lần; update hay thiếu sót hoặc không rõ; advisor phải hỏi lại → mất thêm thời gian 2 chiều. |
| **Success metric** | Có bản update đầy đủ gửi được trong < 10 phút; không bị advisor hỏi lại "tuần này làm gì cụ thể?" trong 4 tuần liên tiếp. |
| **Non-AI alternative** | Daily log tay (ghi 3 dòng mỗi tối về việc đã làm) — giảm bottleneck nhớ lại, nhưng không giải quyết phần tổng hợp thành narrative cho advisor. |
| **AI hypothesis** | AI đọc các nguồn sẵn có (commit message, note, log) → draft bản update theo cấu trúc chuẩn → người dùng review/edit → gửi. |
| **Quick gut** | [x] Workflow |

---
