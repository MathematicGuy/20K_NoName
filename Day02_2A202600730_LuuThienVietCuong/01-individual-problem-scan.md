# 01 — Individual Problem Scan (cá nhân)

## Scan rộng

Tôi scan 10 problems từ trải nghiệm thật trong quá trình đọc paper, ghi chú, so sánh phương pháp và chuẩn bị viết nghiên cứu/luận văn. Tôi ưu tiên các vấn đề có workflow rõ, lặp lại nhiều lần và có dấu hiệu thật.

| # | Lăng kính | Problem quan sát được | Ai đang đau? | Dấu hiệu thật |
|---|---|---|---|---|
| 1 | Lặp lại + Tốn thời gian | Mỗi khi đọc một paper mới tôi phải tự tóm tắt lại mục tiêu, đóng góp, phương pháp và limitation vào ghi chú riêng | Bản thân tôi | 25-45 phút/paper chỉ để hiểu đúng nội dung cốt lõi; nếu đọc nhiều paper thì dễ mất mạch |
| 2 | Tốn thời gian + AI có thể tốt hơn | So sánh nhiều phương pháp cùng một chủ đề (ví dụ quantization, pruning, distillation) vào một bảng tổng hợp | Bản thân tôi | Phải dò từng paper, mỗi paper dùng cách đặt tên và metric khác nhau, rất dễ sót chi tiết |
| 3 | Lặp lại | Truy tìm lại một claim hoặc một con số thí nghiệm đã đọc ở paper cũ | Bản thân tôi | Thường mất 10-20 phút để mở lại PDF, tìm đúng section/figure/table |
| 4 | Pain từ người khác | Khi trình bày paper cho bạn học hoặc nhóm, tôi thường phải giải thích lại cùng một đoạn liên quan đến metric, dataset hoặc giả định | Bạn học, nhóm nghiên cứu | Câu hỏi lặp lại nhiều lần; nếu không chuẩn bị note tốt thì phải trả lời lại từ đầu |
| 5 | Tốn thời gian | Viết related work/literature review đòi hỏi gom nhiều paper rời rạc thành một mạch lập luận thống nhất | Bản thân tôi | Dễ bị đứt mạch, viết xong vẫn phải sửa nhiều vì thiếu logic giữa các nhóm phương pháp |
| 6 | AI có thể tốt hơn | Phân loại paper theo đúng “slot” trong taxonomy của mình: method, dataset, metric, assumption, limitation | Bản thân tôi | Có paper đọc xong vẫn chưa biết nên xếp vào nhóm nào nếu không đối chiếu kỹ |
| 7 | Pain từ người khác | Khi chia sẻ note với bạn khác, họ không hiểu ký hiệu viết tắt hoặc cách tôi rút gọn nội dung | Bạn học, đồng đội | Cần hỏi lại 2-3 lần; note cá nhân không dùng lại được ngay cho người khác |
| 8 | Lặp lại + Tốn thời gian | Chuyển note tiếng Anh từ paper sang câu chữ formal tiếng Việt để dùng trong báo cáo hoặc thuyết trình | Bản thân tôi | Mỗi lần đều phải viết lại từ đầu để tránh diễn đạt quá “dịch máy” |
| 9 | Tốn thời gian | Kiểm tra lại trích dẫn, link nguồn, và định dạng bibliography khi có nhiều paper | Bản thân tôi | Rất dễ thiếu DOI/link, sai tên tác giả, hoặc trích sai nguồn phụ |
| 10 | AI có thể tốt hơn | Rà lại xem một paper có thực sự liên quan đến câu hỏi nghiên cứu của tôi hay chỉ là liên quan bề mặt | Bản thân tôi | Có những paper nhìn rất giống nhưng khác giả định, khác setting hoặc khác target problem |

---

## Top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---|---|---|---|
| 1 | Tóm tắt paper thành note có cấu trúc (#1, #8) | Workflow rõ nhất, xuất hiện gần như mỗi khi đọc paper, và tiết kiệm thời gian trực tiếp | Cách chuẩn hóa note sao cho vừa ngắn vừa không mất ý |
| 2 | So sánh nhiều paper/method vào một bảng luận điểm (#2, #5, #6) | Đây là bước tốn công nhất khi chuẩn bị literature review và slide nghiên cứu | Taxonomy có nên cố định hay thay đổi theo từng đề tài |
| 3 | Truy vết claim, con số và nguồn gốc trích dẫn (#3, #9, #10) | Sai một claim có thể kéo theo sai toàn bộ lập luận, nên giá trị kiểm chứng rất cao | Có nên giải bằng workflow tìm kiếm hay cần một công cụ bán tự động |

---

## Problem Card #1 — Tóm tắt paper thành note có cấu trúc

**Problem 1 câu:**  
Mỗi khi đọc một paper mới, tôi phải tự đọc, tự rút ý và tự viết lại thành note có cấu trúc để có thể dùng lại về sau; bước này tốn nhiều thời gian và dễ làm mất mạch đọc.

**Actor:**  
Bản thân tôi, trong vai trò người học và người làm nghiên cứu.

**Thời điểm / bối cảnh:**  
Khi đọc paper mới, đặc biệt là paper liên quan trực tiếp đến luận văn hoặc đồ án.

**Current workflow 3-7 bước:**  
1. Mở paper và đọc phần abstract, introduction, conclusion.  
2. Đọc tiếp method và experiment để hiểu đóng góp chính.  
3. Tự ghi chú lại mục tiêu, ý chính, limitation, dataset và metric.  
4. Đặt tag hoặc lưu file để sau này có thể tìm lại.  
5. Khi cần dùng lại thì mở note cũ và chỉnh sửa cho phù hợp ngữ cảnh mới.

**Bottleneck:**  
Bước 3, vì tôi phải liên tục chuyển từ “đọc hiểu” sang “viết lại” và thường mất 25-45 phút cho một paper.

**Impact:**  
Tổng thời gian đọc một paper tăng mạnh; nếu đọc nhiều paper trong cùng một chủ đề, phần note chiếm công sức ngang hoặc lớn hơn phần đọc.

**Success metric:**  
Giảm thời gian tạo note từ khoảng 25-45 phút/paper xuống còn 10-15 phút/paper mà vẫn giữ được các trường thông tin quan trọng: mục tiêu, phương pháp, dữ liệu, metric, limitation, và liên hệ với câu hỏi nghiên cứu của tôi.

**Non-AI alternative:**  
Dùng template note cố định hoặc bảng điền tay để ép cấu trúc, nhưng vẫn cần tự đọc và tự viết gần như toàn bộ nội dung.

**AI hypothesis:**  
AI hỗ trợ trích xuất ý chính từ paper và gợi ý note theo template, còn tôi kiểm lại để đảm bảo không mất nghĩa và không chép sai.

**Quick gut:**  
Workflow.

### Draft current workflow

```text
CURRENT STATE — 35 phút trung bình

[1 Mở paper: 2']
→ [2 Đọc abstract/introduction/conclusion: 8']
→ [3 Đọc method/experiment: 12']  <-- hiểu nội dung chính
→ [4 Tự viết note có cấu trúc: 10'] <-- bottleneck
→ [5 Gắn tag/lưu file: 2']
→ [6 Quay lại sửa note nếu cần: 1']
```

### Draft future workflow

```text
FUTURE STATE — 12 phút

[1 Đọc nhanh abstract + figure chính: 3']
→ [2 AI gợi ý note theo template: 2']
→ [3 Tôi kiểm tra lại method/limitation: 4']  <-- human boundary
→ [4 Tôi chỉnh note cuối: 2']
→ [5 Gắn tag/lưu file: 1']

Fallback: AI tóm tắt sai → tôi bỏ output, quay lại viết tay theo template.
```

---

## Problem Card #2 — So sánh nhiều paper/method vào một bảng luận điểm

**Problem 1 câu:**  
Khi chuẩn bị literature review hoặc báo cáo nghiên cứu, tôi phải so sánh nhiều paper cùng chủ đề vào một bảng logic rõ ràng, nhưng mỗi paper lại trình bày theo cách khác nhau nên quá trình tổng hợp rất tốn công.

**Actor:**  
Bản thân tôi.

**Thời điểm / bối cảnh:**  
Khi chốt hướng nghiên cứu, viết related work, hoặc chuẩn bị slide trình bày.

**Current workflow tóm tắt:**  
Đọc từng paper → tự bóc tách method → so metric/dataset/assumption → viết lại thành bảng so sánh → sửa nhiều vòng vì phát hiện chỗ thiếu hoặc chỗ hiểu sai.

**Bottleneck:**  
Bước bóc tách và chuẩn hóa thông tin giữa nhiều paper, vì taxonomy của tôi chưa ổn định và các paper không dùng cùng một ngôn ngữ mô tả.

**Success metric:**  
Giảm thời gian tạo bảng so sánh từ vài giờ xuống dưới 1 giờ cho một cụm paper, đồng thời giữ được ít nhất 5 trường bắt buộc: vấn đề, phương pháp, dữ liệu, metric, limitation.

**Quick gut:**  
Workflow.

### Draft current workflow

```text
CURRENT STATE — 2-3 giờ

[1 Chọn cụm paper: 5']
→ [2 Đọc từng paper: 60-90']
→ [3 Bóc tách method/dataset/metric: 30-45']
→ [4 Tự tạo bảng so sánh: 30-45']  <-- bottleneck
→ [5 Sửa taxonomy và wording: 15-30']
```

### Draft future workflow

```text
FUTURE STATE — 45 phút

[1 Chọn cụm paper và tiêu chí so sánh: 5']
→ [2 AI trích xuất trường chuẩn: 10']
→ [3 Tôi kiểm chéo paper gốc: 15']  <-- human boundary
→ [4 Tôi chỉnh taxonomy và insight: 10']
→ [5 Xuất bảng cuối: 5']

Fallback: nếu paper quá khác nhau, tôi không ép so sánh một bảng, mà tách thành nhiều nhóm nhỏ hơn.
```

---

## Problem Card #3 — Truy vết claim, con số và nguồn gốc trích dẫn

**Problem 1 câu:**  
Tôi thường phải kiểm lại một claim hoặc một con số đã đọc ở paper cũ để dùng vào bài viết, nhưng việc tìm đúng vị trí nguồn gốc trong PDF và kiểm tra lại context rất mất thời gian.

**Actor:**  
Những người có nhu cầu đọc paper (như tôi01-individual-problem-scan.md01-individual-problem-scan.md).

**Thời điểm / bối cảnh:**  
Khi viết báo cáo, related work, hoặc chuẩn bị slide cần dẫn chứng.

**Current workflow tóm tắt:**  
Nhớ đại ý claim → mở lại PDF cũ → tìm keyword → xem bảng/figure/section liên quan → đọc context xung quanh → quyết định có thể trích hay không.

**Bottleneck:**  
Khâu tìm đúng đoạn gốc trong nhiều PDF và xác nhận claim có đúng ngữ cảnh hay không.

**Success metric:**  
Giảm thời gian truy vết từ 10-20 phút xuống còn dưới 5 phút cho một claim, đồng thời giảm rủi ro trích sai ngữ cảnh.

**Quick gut:**  
Workflow.

### Draft current workflow

```text
CURRENT STATE — 15 phút/claim

[1 Nhớ claim mơ hồ: 0']
→ [2 Mở lại paper cũ: 2']
→ [3 Tìm keyword trong PDF: 5']  <-- bottleneck
→ [4 Đọc context quanh chỗ tìm thấy: 5']
→ [5 Kết luận có dùng được không: 3']
```

### Draft future workflow

```text
FUTURE STATE — 4 phút/claim

[1 Tôi lưu claim ngay khi đọc paper: 1']
→ [2 AI hỗ trợ tìm đúng đoạn gốc: 1']
→ [3 Tôi kiểm lại context và số liệu: 1']  <-- human boundary
→ [4 Ghi chú nguồn cuối: 1']

Fallback: nếu không truy vết được, tôi không dùng claim đó.
```

---

## Chọn card muốn pitch nhất

Card tôi muốn pitch nhất:

```text
Problem Card #1 — Tóm tắt paper thành note có cấu trúc
```

Vì sao:

```text
Đây là pain xuất hiện đều nhất trong quá trình học và làm nghiên cứu của tôi. Nó có workflow rõ, có thể đo thời gian, và giải quyết tốt sẽ tạo tác động ngay lập tức cho toàn bộ quá trình đọc paper, viết related work và chuẩn bị nghiên cứu.
```

Câu hỏi tôi muốn nhóm challenge:

```text
Liệu problem này có nên giải bằng AI ở mức workflow hỗ trợ hay chỉ cần một template note thật chặt là đủ? Nếu chỉ dùng AI để tóm tắt, làm sao tránh mất các limitation hoặc giả định quan trọng của paper?
```
