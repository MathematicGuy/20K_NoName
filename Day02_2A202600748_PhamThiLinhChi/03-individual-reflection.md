# Individual Reflection (của Linh Chi)

## Đóng góp của tôi trong nhóm

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng |
|-----------|----------------|----------------------|
| Scan cá nhân | Đưa ra 5 problems về order đồ ăn, workflow chi tiết 25 phút | Nhóm có thêm candidate mạnh về pattern tổng hợp |
| Pitch Problem Card | Trình bày bài order với metric rõ (25 phút/ngày, dễ demo) | Bài vào shortlist, điểm cao thứ hai (32) |
| Challenge bài khác | Hỏi: "Làm sao đảm bảo AI không sinh đáp án nhiễu sai kiến thức?" | Nhóm bổ sung vòng lặp ReAct và boundary rõ |
| Gom trùng / cluster | Đề xuất tách cluster A (sinh nội dung) và B (tổng hợp) | Giúp nhóm chọn đúng cluster A |
| Chọn candidate problem | Ban đầu bảo vệ bài order, sau khi nghe phân tích scale impact đã đổi ý | Nhóm đạt đồng thuận nhanh |
| Validation / research | Tìm info về Zalo Mini App, Splitwise để so sánh | Bổ sung research, thấy rõ khoảng trống của order |
| Problem Statement | Góp ý bổ sung metric chất lượng đáp án nhiễu vào PS v0 | PS trở nên toàn diện hơn |
| Rule / Workflow / Agent | Lập luận bài MCQ nên dùng Workflow, không cần Agent | Nhóm thống nhất chọn Workflow |
| Decision | Đề xuất pilot dùng slide thật, ghi lại thời gian | Giúp nhóm có kế hoạch cụ thể |

## Bảng dùng AI trong reflection

| Phase | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai/hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình |
|-------|------------------------|-------------------|----------------------|-----------------------------------|
| Scan | Nhờ ChatGPT gợi ý problems về quản lý order | Có thêm ý "dự trù giờ order", "nhập menu từ ảnh" | AI đề xuất "tự động gọi điện cho quán" – không thực tế | Bỏ qua, chỉ giữ ý khả thi |
| Problem Card | Dùng AI format workflow thành bảng | Nhanh, dễ đọc | AI tự thêm bước "gửi email xác nhận" – không có thật | Xóa bước đó |
| Research | Tìm giải pháp order nhóm có tích hợp AI | Gợi ý Misa Munch, Zalo Mini App | AI nói "Zalo Mini App parse free text" – kiểm tra thì không | Chỉ giữ thông tin đã verify |
| Workflow | Nhờ AI vẽ Mermaid cho future workflow order | Dễ hình dung | AI bỏ bước "HR kiểm tra" – coi như AI tự gửi order | Tôi tự thêm bước Human review |
| Problem Statement | Dùng AI phản biện PS v0 | AI chỉ ra cần thêm metric chất lượng đáp án | AI đề xuất thay vòng lặp bằng tự động duyệt – nguy hiểm | Tôi bỏ qua, giữ vòng lặp ReAct |

## Câu hỏi mở – Reflection

**Tôi học được gì khi nghe top 3 problems của các bạn khác?**

Tôi học được rằng một bài toán tưởng "nhỏ" (order đồ ăn) có thể rất mạnh về độ rõ ràng, nhưng khi so sánh về scale impact, bài toán MCQ lại vượt trội hơn hẳn. Điều này dạy tôi rằng không chỉ nhìn vào độ khó hay độ "cool" của AI, mà còn phải nhìn vào số người được giúp đỡ và tần suất lặp lại.

**Nhóm có lúc nào bị solution-first không?**

Có, khi tôi pitch bài order, tôi đã nói ngay "dùng AI parse free text" mà chưa phân tích kỹ xem liệu rule (form) có đủ không. Câu hỏi "Nếu chỉ cần dùng Google Form thì AI có còn cần không?" giúp tôi nhận ra mình đang solution-first.

**Tôi có thay đổi ý kiến sau khi bị challenge không?**

Có. Ban đầu tôi rất tự tin với bài order vì nó gần gũi. Nhưng khi nghe phân tích về scale impact: 20 giảng viên mỗi người tiết kiệm 2 giờ/tuần sẽ gấp nhiều lần 1 HR tiết kiệm 40 phút/ngày, tôi thấy không thể phản bác. Tôi đã bỏ phiếu cho bài MCQ.

**Tôi đóng góp gì thật sự vào artifact cuối?**

Tôi đóng góp vào việc phản biện làm rõ rủi ro của AI (hallucination), đề xuất bổ sung metric chất lượng cho PS, và thúc đẩy nhóm chọn Workflow thay vì Agent. Dù bài của tôi không được chọn, nhưng những đóng góp của tôi giúp bài MCQ trở nên chắc chắn hơn.

**Điều khó nhất khi viết Problem Statement là gì?**

Khó nhất là định nghĩa success metric cho "chất lượng" – không chỉ thời gian mà còn độ hài lòng của giảng viên với đáp án nhiễu. Nhóm đã giải quyết bằng cách thêm khảo sát Likert 5 điểm sau khi chỉnh sửa.

**Nếu làm lại, tôi sẽ challenge nhóm mạnh hơn ở điểm nào?**

Tôi sẽ challenge mạnh hơn về khả năng tích hợp thực tế của giải pháp MCQ vào LMS của trường. Nếu trường dùng Moodle thì GIFT là chuẩn, nhưng nếu dùng hệ thống khác thì sao? Lẽ ra tôi nên hỏi câu đó ngay từ đầu.

## Self-Check Cuối Bài

### Nhóm
- [15đ] Workflow trước/sau chi tiết: Có bảng + Mermaid, thể hiện rõ actor, bottleneck, AI intervention point.
- [20đ] Problem Statement v0/v1: Đủ 6 field + metric đo được + boundary rõ.
- [15đ] So sánh Rule/Workflow/Agent: Có ma trận + lý do chọn/không chọn.
- [10đ] Decision Go/Not Yet/No-Go: Có bảng kiểm + lý do dựa trên evidence.
- [+10 bonus] Scan rộng + tương tác tích cực + research vượt yêu cầu.

### Cá nhân (Linh Chi)
- [12đ] Có 5+ problems và top 3 Problem Cards.
- [12đ] Pitch rõ và challenge nhóm đúng trọng tâm.
- [10đ] Reflection nói rõ vai trò, cách dùng AI, bài học, nếu làm lại sẽ đổi gì.
- [6đ] Tự giải thích được mạch: problem → workflow → metric → boundary → độ phù hợp AI.
