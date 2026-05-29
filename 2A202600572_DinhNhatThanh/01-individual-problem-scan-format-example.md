# 01 — Individual Problem Scan (cá nhân)

## Scan rộng

Tôi scan 10 problems từ trải nghiệm thật hàng ngày, đa dạng lăng kính.

| # | Lăng kính | Problem quan sát được | Ai đang đau? | Dấu hiệu thật |
|---|---|---|---|---|
| 1 | Lặp lại + Tốn thời gian | Mỗi trưa phải hỏi khắp team "ăn gì? order chung không?" rồi tổng hợp món | Cả team (5-7 người) | Mất 15-20 phút mỗi ngày, tin nhắn lộn xộn, hay người quên reply |
| 2 | Tốn thời gian + Lặp lại | Tự mở các app (Grab, ShopeeFood, BeFood, BAEMIN) so sánh giá/món để tìm tốt nhất | Cá nhân người order | Mỗi lần order mất 5-10 phút chuyển app, có ngày phải làm 2-3 lần |
| 3 | AI có thể tốt hơn | Nhập món từ ảnh chụp menu (quán mới, order qua Zalo) vào app một cách thủ công | Người order | Hay gõ sai tên món, thiếu topping, phải gửi lại 2-3 lần |
| 4 | Pain từ người khác | Người trong team than "order trễ quá, 12h30 mới có đồ", "sao giao thiếu món của tôi" | Cả team | Có người bỏ order giữa chừng, hoặc tự đi ăn riêng |
| 5 | Lặp lại | Tính tiền và chia bill sau khi nhận đồ: ai ăn gì, giá bao nhiêu, ship bao nhiêu, ai chưa chuyển khoản | Người order, kế toán team | Mất 10-15 phút sau mỗi bữa, phải hỏi lại nhiều lần |
| 6 | Tốn thời gian | Gọi điện hoặc nhắn tin riêng cho quán để xác nhận đơn (vì app không lấy được hết món) | Người order | Mất thêm 5 phút, dễ sai số điện thoại |
| 7 | AI có thể tốt hơn | Order quán quen nhưng không lưu được món ưa thích của từng người, mỗi lần phải hỏi lại "Nam ăn gì? Ly uống gì?" | Người order, cả team | Lãng phí thời gian hỏi lại, nhiều người trả lời chậm |
| 8 | Pain từ người khác | Người mới vào team không biết quy trình order, hỏi lại "mình order ở đâu? ship thế nào?" | Người order (onboarding lặp lại) | Mất 5-10 phút giải thích mỗi khi có người mới |
| 9 | Lặp lại + Tốn thời gian | Phải dự trù giờ order để đồ về đúng 12h, nhưng thường xuyên sai (sớm quá hoặc trễ quá) | Người order, người đói | Đồ để nguội hoặc phải chờ thêm 20 phút |
| 10 | AI có thể tốt hơn | Khi có người đổi ý món hoặc thêm trễ, không có cách nào cập nhật đơn một cách thông minh | Người order, quán | Phải nhắn lại riêng với quán, dễ gây sai sót |

---

## Top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---|---|---|---|
| 1 | Tổng hợp order + tính tiền (#1, #5, #7) | Workflow rõ nhất, mất thời gian lớn nhất (20-30 phút/ngày), nhiều người đau | Liệu AI có thể hiểu các món free text không? |
| 2 | So sánh giá/món giữa các app (#2) | Tốn thời gian cá nhân, có thể giải quyết bằng AI tổng hợp | Dữ liệu từ các app khó lấy tự động, scope lớn |
| 3 | Xác nhận đơn với quán (#6, #10) | Có pain thật (giao thiếu, sai món), AI giúp chuẩn hóa tin nhắn | Phụ thuộc vào quán bên ngoài |

---

## Problem Card #1 — Tổng hợp order trưa

**Problem 1 câu:**  
Mỗi ngày, người chịu trách nhiệm order (luân phiên) mất khoảng 20-30 phút để hỏi team, tổng hợp món, tính tiền và chia bill, gây trễ giờ ăn và ức chế.

**Actor:**  
Thành viên trong team (5-7 người) đến lượt order. Không có role cố định.

**Thời điểm / bối cảnh:**  
Khoảng 11h-11h30 hàng ngày, trước giờ ăn trưa.

**Current workflow:**

```text
1. Hỏi trong group chat "hôm nay ăn gì? ai order chung?"
2. Chờ mọi người đề xuất món/quán (5-10 phút)
3. Tổng hợp các món (người A: cơm tấm, B: bún bò, C: trà đào...)
4. Gửi danh sách cho quán (qua Zalo/Grab)
5. Khi đồ đến, tính tiền từng người (giá món + chia ship)
6. Thông báo số tiền và chờ chuyển khoản
7. Đối chiếu ai chưa chuyển (có khi nhắc lại sau)
```

**Bottleneck:**  
Bước 3 (tổng hợp món) và bước 5 (tính tiền) mất nhiều thời gian vì nhập tay, dễ nhầm.

**Impact:**  
20-30 phút/ngày × 5 ngày = 100-150 phút/tuần cho người order. Cả team ăn trễ, căng thẳng nhẹ.

**Success metric:**  
Giảm thời gian từ khi bắt đầu hỏi đến khi gửi order xong xuống dưới 10 phút. Giảm số lần hỏi lại "bạn ăn gì?" xuống 0.

**Non-AI alternative:**  
Google Form hoặc bảng tính shared. Nhưng mọi người ngại mở link, vẫn thích nhắn chat.

**AI hypothesis:**  
AI đọc tin nhắn (hoặc form nhập tự do), trích xuất tên người + món + số lượng, tự động tính tiền dựa trên giá đã biết hoặc tra nhanh.

**Quick gut:**  
Workflow.

### Draft current workflow

```text
CURRENT STATE — 25 phút (trung bình)

[1 Hỏi team: 2']
→ [2 Chờ đề xuất: 10']  <-- chờ người chậm
→ [3 Tổng hợp món (gõ tay): 5']
→ [4 Gửi quán: 2']
→ [5 Tính tiền + chia ship: 5']
→ [6 Thông báo + thu tiền: 1']
→ (Có khi bước 7 nhắc nợ: +2')
```

### Draft future workflow

```text
FUTURE STATE — 10 phút

[1 AI hỏi tự động (hoặc form): 0']  -- thay thế bước chờ
[2 Mọi người reply món (free text): 5']  <-- vẫn chờ người
[3 AI parse và tổng hợp món: 1']
[4 AI tính tiền + ship: 1']
[5 Người order kiểm tra và gửi quán: 3']  <-- human boundary

Fallback: AI parse sai → người sửa thủ công.
```

---

## Problem Card #2 — So sánh giá giữa các app

**Problem 1 câu:**  
Mỗi lần order, người order mất 5-10 phút mở đi mở lại 3-4 app giao đồ ăn để so sánh giá và khuyến mãi cho cùng một món/quán.

**Actor:**  
Người order bất kỳ.

**Current workflow tóm tắt:**  
Mở Grab → gõ tên món → xem giá → chụp màn hình → mở ShopeeFood → gõ lại → so sánh → quyết định.

**Bottleneck:**  
Phải nhập lại tên món nhiều lần, không có view tổng hợp.

**Success metric:**  
Giảm từ 5-10 phút xuống dưới 1 phút cho mỗi lần so sánh.

**Quick gut:**  
Agent (cần crawl dữ liệu) hoặc Workflow phức tạp.

---

## Problem Card #3 — Xác nhận đơn với quán

**Problem 1 câu:**  
Sau khi gửi đơn qua Zalo/messenger, người order thường phải gọi điện hoặc nhắn lại để xác nhận, mất 5 phút và dễ sai sót.

**Actor:**  
Người order.

**Current workflow tóm tắt:**  
Soạn tin nhắn danh sách món → gửi → chờ 2-3 phút → nếu không reply thì gọi → đọc lại danh sách.

**Bottleneck:**  
Không có cơ chế xác nhận tự động; quán bận không rep kịp.

**Success metric:**  
Giảm thời gian xác nhận xuống dưới 30 giây, không cần gọi điện.

**Quick gut:**  
Workflow (tạo template tin nhắn có cấu trúc + tự động nhắc nếu không phản hồi).

