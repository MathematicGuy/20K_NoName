# 01 — Individual Problem Scan (cá nhân - 2A202600572 - Đinh Nhật Thanh)

## Scan rộng

Tôi scan 10 problems từ trải nghiệm thực tế trong công tác giảng dạy và quản lý học thuật của Giảng viên đại học, đa dạng lăng kính.

| # | Lăng kính | Problem quan sát được | Ai đang đau? | Dấu hiệu thật |
|---|---|---|---|---|
| 1 | Lặp lại + Tốn thời gian | Thiết kế và soạn bộ câu hỏi trắc nghiệm (MCQ) từ slide bài giảng định kỳ | Giảng viên, trợ giảng | Mất 120-180 phút/tuần cho mỗi bộ quiz |
| 2 | Lặp lại | Copy/paste điểm thi và format bảng điểm từ các file Excel vào hệ thống Portal của trường | Giảng viên | Lặp lại mỗi đợt thi, mất 30 phút/lớp |
| 3 | Tốn thời gian | Chấm bài tập lớn/đồ án dài của sinh viên và viết nhận xét chi tiết theo tiêu chí chấm (rubric) | Giảng viên | Mất 45 phút/nhóm báo cáo |
| 4 | Pain từ người khác | Trả lời các câu hỏi lặp đi lặp lại của sinh viên về quy chế, deadline, đề cương trên Zalo/Teams | Giảng viên, Sinh viên | Xuất hiện hàng ngày, trôi tin nhắn |
| 5 | Tốn thời gian | Viết phần tổng quan nghiên cứu (Literature Review) cho bài báo khoa học bằng cách tổng hợp hàng chục bài nghiên cứu tiếng Anh | Giảng viên nghiên cứu | Mất 2-3 tuần cho một bản nháp |
| 6 | Tốn thời gian | Soạn slide bài giảng mới từ sách giáo trình dày hơn 500 trang | Giảng viên | Mất 120-180 phút/chương |
| 7 | Lặp lại + Tốn thời gian | Soạn giáo án và đề cương chi tiết môn học (Syllabus) để map các chuẩn đầu ra (CLO) với bài tập đánh giá | Giảng viên, trưởng bộ môn | Mất 240 phút/đề cương mỗi học kỳ |
| 8 | AI có thể tốt hơn | Đối chiếu báo cáo đạo văn Turnitin để lọc ra các trích dẫn đúng chuẩn thay vì quy kết đạo văn | Giảng viên | Mất 20 phút/báo cáo |
| 9 | Lặp lại | Soạn và gửi các thông báo nhắc nộp bài, lịch học bù, nghỉ học qua email và Portal | Giảng viên | Mất 10-15 phút/lần thông báo |
| 10| AI có thể tốt hơn | Phân chia nhóm sinh viên làm bài tập lớn dựa trên khảo sát trình độ và đăng ký đề tài rời rạc | Giảng viên | Mất 60 phút/lớp đông |

---

## Top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---|---|---|---|
| 1 | Tạo câu hỏi trắc nghiệm (MCQ) (#1) | Quy trình các bước rất rõ ràng, là việc lặp đi lặp lại hàng tuần, tốn nhiều thời gian và công sức sáng tạo đáp án nhiễu (distractors). Có metric đo lường rõ rệt. | Làm sao đo lường độ khó và đảm bảo AI không sinh ra kiến thức sai lệch (hallucination). |
| 2 | Chấm bài luận/đồ án lớn (#3) | Là nỗi đau lớn nhất cuối mỗi học kỳ, tốn cực kỳ nhiều năng lượng để đọc hiểu và viết nhận xét khách quan. | Tính công bằng và cá nhân hóa của nhận xét do AI hỗ trợ nháp. |
| 3 | Trả lời câu hỏi sinh viên lặp lại (#4) | Tần suất xuất hiện hàng ngày, gây đứt gãy công việc nghiên cứu và chuẩn bị bài giảng của giảng viên. | Cách tích hợp an toàn vào các kênh chat của trường và kiểm soát bảo mật thông tin sinh viên. |

---

## Problem Card #1 — Soạn câu hỏi trắc nghiệm (MCQ) cho Giảng Viên

**Problem 1 câu:**  
Mỗi tuần giảng viên mất từ 120-180 phút để soạn bộ câu hỏi trắc nghiệm chất lượng cao từ slide bài giảng, trong đó bước sáng tạo ra các phương án nhiễu (distractors) khoa học, plausibility hợp lý tốn nhiều công sức nhất và định dạng xuất ra LMS dễ gặp lỗi cú pháp.

**Actor:**  
Giảng viên đại học phụ trách các môn học lý thuyết cần kiểm tra định kỳ bằng hình thức trắc nghiệm.

**Thời điểm / bối cảnh:**  
Cuối mỗi tuần sau buổi học hoặc trước các đợt thi giữa kỳ, cuối kỳ.

**Current workflow:**
1. Đọc và hệ thống hóa lại nội dung slide bài giảng của tuần.
2. Lọc ra các khái niệm, định nghĩa cốt lõi cần kiểm tra (nhớ, hiểu, vận dụng).
3. Viết câu hỏi (question stem) cho khái niệm đó.
4. Xác định đáp án đúng (correct key).
5. Sáng tạo 3 đáp án nhiễu (distractors) sao cho khoa học, có vẻ hợp lý nhưng sai hoàn toàn để phân loại học sinh (tránh đáp án hiển nhiên sai).
6. Định dạng thủ công bộ câu hỏi theo chuẩn Aiken hoặc GIFT để chuẩn bị import vào LMS (Moodle, Canvas).
7. Đăng tải lên LMS và thực hiện test thử đề thi.

**Bottleneck:**  
Bước 5 (nghĩ đáp án nhiễu) mất nhiều thời gian nhất vì cần tính tư duy cao, và bước 6 (định dạng chuẩn LMS) dễ gây lỗi cú pháp hệ thống.

**Impact:**  
Mất 120-180 phút/tuần cho mỗi giảng viên. Một khoa có 20 giảng viên tiêu tốn khoảng 40-60 giờ/tuần chỉ làm công việc hành chính này. Báo cáo đề thi trễ hoặc đề thi chất lượng kém (đáp án nhiễu quá dễ đoán) làm mất tính khách quan và tính phân loại của bài thi.

**Success metric:**  
Giảm tổng thời gian biên soạn đề từ 120 phút xuống dưới 25 phút cho mỗi bộ 20 câu hỏi; tỷ lệ lỗi cú pháp định dạng khi import LMS bằng 0.

**Non-AI alternative:**  
Sử dụng lại ngân hàng đề thi cũ của những năm trước hoặc dùng đề trắc nghiệm đi kèm sách giáo khoa của nhà xuất bản. Nhưng phương án này không bám sát nội dung slide cập nhật thực tế trên lớp.

**AI hypothesis:**  
AI hỗ trợ đọc slide bài giảng, tự động lọc khái niệm then chốt để đề xuất câu hỏi, đáp án đúng và 3 đáp án nhiễu thông minh. Giảng viên đóng vai trò là "chốt chặn kiểm soát" (human-in-the-loop) để chọn lọc và biên tập trực tiếp. Sau đó hệ thống tự động xuất file GIFT/Aiken chuẩn hóa mà không có lỗi format.

**Quick gut:**  
Workflow.

### Draft current workflow

```text
CURRENT STATE — 120 phút (cho 20 câu trắc nghiệm)

[1 Đọc slide bài giảng: 20']
→ [2 Xác định khái niệm kiểm tra: 15']
→ [3 Viết câu hỏi & đáp án đúng: 25']
→ [4 Nghĩ ra 3 đáp án nhiễu chất lượng: 40']  <-- bottleneck chính (viết nội dung)
→ [5 Định dạng chuẩn Aiken/GIFT: 15']         <-- bottleneck kỹ thuật (định dạng)
→ [6 Upload LMS & test: 5']
```

### Draft future workflow

```text
FUTURE STATE — 25 phút (cho 20 câu trắc nghiệm)

[1 Upload slide bài giảng lên hệ thống: 1']
→ [2 AI trích xuất khái niệm & draft câu hỏi + đáp án nhiễu: 2']    -- AI workflow step
→ [3 Giảng viên xem, chọn lọc & chỉnh sửa (Human-in-the-Loop): 18']  <-- human boundary
→ [4 AI tự động định dạng chuẩn hóa Aiken/GIFT bằng code: 1']        -- Rule/script step
→ [5 Giảng viên download file sạch & import trực tiếp lên LMS: 3']

Fallback: AI sinh đáp án bịa đặt/sai kiến thức -> Giảng viên từ chối nháp và quay lại viết thủ công dựa trên template Word có sẵn.
```

---

## Problem Card #2 — Chấm bài tập lớn/đồ án

**Problem 1 câu:**  
Mỗi cuối học kỳ, giảng viên tốn khoảng 45 phút cho mỗi nhóm đồ án để đọc hiểu báo cáo dài 15-20 trang và viết nhận xét chi tiết, công bằng dựa trên rubric, gây kiệt sức và quá tải.

**Actor:**  
Giảng viên đại học trực tiếp chấm bài tập lớn/đồ án môn học.

**Current workflow tóm tắt:**  
Đọc báo cáo đồ án của nhóm (15-20 trang) → Đối chiếu từng tiêu chí trong rubric → Ghi điểm cho từng tiêu chí → Viết đoạn nhận xét chi tiết về ưu/nhược điểm và hướng cải thiện cho từng nhóm → Nhập điểm vào bảng tổng hợp.

**Bottleneck:**  
Đọc hiểu nhanh báo cáo dài và viết đoạn nhận xét cá nhân hóa chất lượng cao mà không bị lặp khuôn từ bài này sang bài khác.

**Success metric:**  
Giảm thời gian chấm và nhận xét từ 45 phút xuống dưới 15 phút cho mỗi nhóm đồ án mà vẫn giữ nguyên chất lượng phản hồi hữu ích cho sinh viên.

**Quick gut:**  
Workflow.

---

## Problem Card #3 — Trả lời câu hỏi sinh viên lặp lại

**Problem 1 câu:**  
Giảng viên mất khoảng 15 phút mỗi ngày để tìm kiếm thông tin cũ và trả lời đi trả lời lại các câu hỏi giống nhau của sinh viên về quy chế, deadline và đề cương trên group chat lớp (Zalo/Teams).

**Actor:**  
Giảng viên chủ nhiệm hoặc giảng viên lý thuyết môn học.

**Current workflow tóm tắt:**  
Sinh viên nhắn tin hỏi trên group chat → Giảng viên đọc tin nhắn → Tìm lại file đề cương/thông báo cũ trên máy hoặc Portal → Copy thông tin hoặc gõ câu trả lời → Gửi vào group chat.

**Bottleneck:**  
Tìm kiếm thông tin cũ và gõ lại câu trả lời trong khi đang làm các công việc chuyên môn khác, gây gián đoạn sự tập trung.

**Success metric:**  
Giảm thời gian phản hồi câu hỏi lặp lại xuống dưới 2 phút mỗi ngày, tự động nhắc nhở sinh viên tự tra cứu trước khi hỏi.

**Quick gut:**  
Workflow.
