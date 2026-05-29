# Case Study: Tổng hợp đánh giá phỏng vấn
*Interview Feedback Synthesis — Use Case cho AI Workflow Automation*

---

## Bối cảnh

**Nhân vật:** Lan — HR / Talent Acquisition Executive tại một công ty Tech quy mô ~150 người.

Mỗi tuần có khoảng 10–15 buổi phỏng vấn. Lan thu thập nhận xét từ các Tech Lead qua Slack, Email hoặc note rời rạc, sau đó tổng hợp thành báo cáo chuẩn trên Notion để Hiring Manager ra quyết định.

---

## Vì sao đây là ví dụ tốt?

- **Có actor cụ thể:** HR Executive và Tech Leads.
- **Workflow lặp lại hằng tuần:** Nhắc nhở nộp feedback → Đọc → Tóm tắt → Format → Đăng lên hệ thống.
- **Bottleneck rõ ràng:** Đợi Tech Lead viết feedback lâu, mỗi người viết một kiểu — người tiếng Anh, người tiếng Việt, người gạch đầu dòng vắn tắt.
- **Metric thời gian đo được:** 30–45 phút để "đòi" và tổng hợp cho mỗi ứng viên.
- **Before/After workflow rõ:** Dễ áp dụng AI để đọc data thô và map vào template chuẩn.

---

## 01 — Individual Problem Scan

Lan scan 10 problems trong công việc hằng ngày.

| # | Lăng kính | Problem quan sát được | Ai đang đau? | Dấu hiệu thật |
|---|---|---|---|---|
| 1 | Lặp lại | Trả lời câu hỏi lặp lại về chính sách nghỉ phép, bảo hiểm cho nhân viên mới | HR, Nhân viên mới | Mất 15–20 phút/ngày gõ lại cùng một câu trả lời trên Slack |
| 2 | Tốn thời gian | Đọc lướt và sàng lọc hàng chục CV từ các platform tuyển dụng để tìm keyword | HR | 1–2 tiếng/ngày vào mùa tuyển dụng cao điểm |
| 3 | Lặp lại | Soạn email từ chối gửi ứng viên sau khi rớt phỏng vấn | HR | Lặp lại hàng tuần, mất 30 phút đổi tên và vị trí ứng tuyển |
| 4 | Tốn thời gian | **Thu thập, đọc và tổng hợp feedback phỏng vấn từ các Tech Lead lộn xộn** | HR, Hiring Manager | Mất 30–45 phút/ứng viên. Manager hay phàn nàn vì đọc feedback khó hiểu |
| 5 | AI có thể tốt hơn | Set lịch phỏng vấn: check chéo lịch Google Calendar của 2–3 Tech Lead và ứng viên | HR, Người phỏng vấn | 15–20 phút/lần set lịch. Hay bị trùng lịch phải hẹn lại |
| 6 | Pain từ người khác | Ứng viên phàn nàn công ty thông báo kết quả chậm do HR bận chưa kịp tổng hợp feedback | Ứng viên, HR | Rớt 10–15% ứng viên tiềm năng do họ nhận offer công ty khác trước |
| 7 | Lặp lại | Điền thông tin nhân viên mới vào các file hợp đồng lao động (Word template) | HR | 15 phút/hợp đồng. Dễ sai sót đánh máy tên hoặc lương |
| 8 | Pain từ người khác | Kế toán và HR phải nhắc từng người nộp timesheet / claim chi phí vào ngày cuối tháng | HR, Kế toán, Nhân sự | Mất cả buổi chiều cuối tháng nhắn tin nhắc nhở từng người |
| 9 | Tốn thời gian | Tạo quy trình onboarding, cấp quyền truy cập các tool (Jira, Slack, Email) cho người mới | IT, HR | Mất 1 tiếng/nhân sự mới, đôi khi cấp sót quyền |
| 10 | AI có thể tốt hơn | Chấm điểm bài test văn hóa / tính cách của ứng viên để đánh giá mức độ phù hợp | HR | Khó đánh giá khách quan, tốn nhiều thời gian đọc câu trả lời tự luận |

