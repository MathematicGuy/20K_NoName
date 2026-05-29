# 03 — Individual Reflection

## Đóng góp trong nhóm

| Hoạt động | Hieu đã làm gì? | Kết quả |
|---|---|---|
| Scan cá nhân | Scan 10 problems theo nhiều lăng kính, đưa ra Top 3 candidates | Nhóm có candidates rõ về học tập / nghiên cứu cá nhân |
| Pitch | Pitch 3 problems: đọc paper, theo dõi deadline, update advisor | Nhóm có cơ sở để so sánh và chọn bài |
| Workflow | Vẽ current/future workflow cho cả 3 problem cards dạng ASCII và SVG | Nhóm thấy rõ bottleneck và điểm AI can thiệp |
| Rule / Workflow / Agent | Lập luận loại Card #3 (log experiment) vì MLflow/W&B đã đủ mạnh; giữ lại Card về update advisor thay thế | Tránh chọn problem mà Non-AI alternative đã giải quyết tốt |
| Rule / Workflow / Agent | Lập luận Card #2 (deadline) chọn Rule thay vì Workflow vì logic rành mạch, không cần AI | Nhóm phân biệt được khi nào Rule đủ, khi nào mới cần Workflow |

---

## Bảng dùng AI trong quá trình làm bài

| Phase | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai/hời hợt ở đâu? | Tôi sửa gì |
|---|---|---|---|---|
| Scan | Nhờ AI gợi ý thêm problems theo lăng kính "lặp lại" và "dễ bỏ sót" trong lĩnh vực học tập | Giúp nhớ thêm các pain points ít rõ ràng hơn như chuẩn bị câu hỏi trước seminar, ghi lại kết quả thực nghiệm | AI gợi ý một số ý quá chung chung, không có actor hoặc workflow thật | Bỏ các ý không có dấu hiệu thật hoặc đã có Non-AI alternative rõ ràng |
| Chọn Top 3 | Nhờ AI phân tích lý do nên loại problem nào | Chỉ ra nhanh các problem mà Non-AI alternative đã đủ mạnh (setup môi trường, log experiment) | AI ban đầu giữ lại problem log experiment mà không chú ý MLflow đã giải quyết | Tự phát hiện và loại Card #3 ban đầu, thay bằng problem update advisor |
| Workflow | Nhờ AI vẽ workflow ASCII before/after cho từng card | Draft nhanh được cấu trúc bước, ước lượng thời gian từng bước hợp lý | AI đôi khi gộp bước bottleneck và bước thường vào một, làm mờ điểm nghẽn chính | Tách lại rõ ràng, đánh dấu bottleneck và AI step riêng biệt |
| Vẽ sơ đồ | Nhờ AI vẽ SVG workflow và overview diagram | Tiết kiệm thời gian so với vẽ tay; sơ đồ rõ màu, có phân biệt bottleneck/AI step/human boundary | Tọa độ SVG đôi khi bị overlap nếu không kiểm tra kỹ | Review lại từng sơ đồ, yêu cầu AI điều chỉnh khi phát hiện lỗi layout |
| Lập luận R/W/A | Nhờ AI phản biện lựa chọn Workflow cho Card #1 và #3 | Chỉ ra điều kiện để Workflow hợp lý hơn Rule: có bước ngôn ngữ/tổng hợp mà Rule không xử lý được | AI đề xuất Agent cho Card #3 (update advisor) vì "nhiều nguồn dữ liệu" — không cần thiết | Giữ Workflow vì luồng cố định, chỉ cần AI ở một bước cụ thể, không cần tự lập kế hoạch động |

---

## Bài học

- **Non-AI alternative là bộ lọc quan trọng nhất.** Problem tốt không phải problem nghe "AI" nhất, mà là problem mà giải pháp thủ công hoặc Rule chưa đủ giải quyết phần ngôn ngữ/tổng hợp. Log experiment (MLflow) và setup môi trường (script) đều bị loại vì lý do này.

- **Rule không thua kém Workflow hay Agent.** Card #2 (deadline) chọn Rule là lựa chọn tối ưu, không phải lựa chọn "chưa đủ tham vọng". Giải pháp đơn giản nhất giải quyết được bài toán là giải pháp tốt nhất.

- **Vẽ workflow giúp thấy rõ AI nên đứng ở đâu.** Trước khi vẽ, bước "tổng hợp narrative" trong Card #3 nghe có vẻ đơn giản. Sau khi vẽ, mới thấy đây là điểm duy nhất Rule không làm được — giúp xác định đúng AI intervention point thay vì ôm toàn bộ workflow.

- **Agent không phải đích đến mặc định.** Cả 3 card đều không chọn Agent vì workflow có luồng cố định và cần human review rõ ràng. Agent chỉ hợp khi không thể xác định trước các bước thực thi.

Nếu làm lại:

```
Tôi sẽ validate con số thời gian (30–60 phút/paper, 45 phút/update)
với người khác có cùng workflow trước khi chốt metric,
vì baseline hiện tại chủ yếu đến từ quan sát của bản thân.
```

---

*Bản nộp cá nhân — Day 02 Lab*