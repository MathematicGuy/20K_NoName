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

---Dưới đây là 2 problem card bổ sung (#4 và #5) từ danh sách scan ban đầu, để bạn có thêm lựa chọn khi nhóm hội tụ.

---

## Problem Card #4 — Dự trù giờ order bị sai

**Problem 1 câu:**  
Người order thường xuyên tính sai thời gian giao hàng (sớm quá hoặc trễ quá) so với 12h trưa, làm đồ nguội hoặc cả team phải chờ, gây lãng phí thời gian và ảnh hưởng tinh thần.

**Actor:**  
Người order (luân phiên).

**Thời điểm / bối cảnh:**  
Trước khi gửi order (khoảng 11h), phải ước lượng: quán nấu bao lâu, shipper lấy và di chuyển bao lâu.

**Current workflow:**

```text
1. Nhớ lại kinh nghiệm lần trước (nếu quán quen)
2. Hoặc đoán: "chắc 30 phút"
3. Quyết định gửi order lúc 11h15 nếu đoán 45 phút giao
4. Thực tế: hôm thì 11h45 đã có (đồ nguội), hôm thì 12h15 mới có (cả team đói)
```

**Bottleneck:**  
Không có dữ liệu thực tế về thời gian giao hàng theo quán, theo khung giờ, theo app. Phụ thuộc vào cảm tính.

**Impact:**  
Trung bình mỗi tuần 2-3 bữa bị lệch hơn 15 phút so với mong muốn. Mỗi lần cả team mất khoảng 5-10 phút chờ hoặc than phiền.

**Success metric:**  
Giảm tỷ lệ bữa ăn bị trễ >15 phút từ ~40% xuống dưới 10%. Hoặc giảm thời gian chờ trung bình từ 12 phút xuống 5 phút.

**Non-AI alternative:**  
Ghi chép thủ công thời gian giao của từng quán vào bảng, tính trung bình. Nhưng không ai làm vì lười và mỗi lần điều kiện khác nhau.

**AI hypothesis:**  
AI học từ lịch sử order (ngày, giờ, quán, app) để dự đoán thời gian giao tối ưu, gợi ý thời điểm nên gửi order. Hoặc tích hợp API thời gian thực từ app (nếu có).

**Quick gut:**  
Workflow + Rule (thống kê đơn giản) có thể đủ nếu có dữ liệu. AI chỉ cần nếu muốn dự đoán theo nhiều biến số.

---

## Problem Card #5 — Order trễ gây ức chế và rủi ro social

**Problem 1 câu:**  
Khi order bị trễ (do tính sai giờ, quán chậm, shipper lạc), người order phải chịu áp lực từ team (càm ràm, hỏi "sắp có chưa") trong khi không thể làm gì nhanh hơn.

**Actor:**  
Người order (đặc biệt là người mới hoặc người ít nói).

**Thời điểm / bối cảnh:**  
Từ lúc dự kiến có đồ (12h) đến khi đồ thực sự đến (12h15-12h30).

**Current workflow:**

```text
1. Nhận câu hỏi "đến đâu rồi?" từ 2-3 người
2. Mở app check tình trạng shipper
3. Trả lời "sắp rồi" (dù không biết chính xác)
4. Lặp lại mỗi 5 phút
5. Cảm thấy có lỗi dù không phải lỗi của mình
```

**Bottleneck:**  
Không có cơ chế cập nhật trạng thái tự động cho cả team. Người order trở thành "màn hình hiển thị" thủ công.

**Impact:**  
Stress tinh thần cho người order, ảnh hưởng đến không khí team (cáu gắt nhẹ). Có thể dẫn đến việc người từ chối order khi đến lượt.

**Success metric:**  
Giảm số câu hỏi "đến đâu rồi?" xuống gần 0. Người order không còn cảm thấy áp lực.

**Non-AI alternative:**  
Share link theo dõi đơn hàng từ Grab/ShopeeFood vào group chat. Nhưng mỗi lần phải copy link, và có người không biết xem.

**AI hypothesis:**  
AI tự động lấy trạng thái từ app (nếu có API) hoặc từ ảnh chụp màn hình của người order, sau đó broadcast vào group chat mỗi khi có thay đổi (đã lấy hàng, đang giao, cách 5 phút). Hoặc AI trả lời tự động các câu hỏi "đến đâu rồi?" bằng cách tổng hợp thông tin.

**Quick gut:**  
Workflow (tự động share link) + Rule (nhắc người order làm vài thao tác đơn giản). AI không thực sự cần nếu các app đã có tracking.

---

## Tóm tắt các Problem Cards (1-5)

| Card | Problem chính | Bottleneck chính | Success metric | Quick gut |
|---|---|---|---|---|
| #1 | Tổng hợp món + tính tiền | Gom món thủ công, chia tiền mất thời gian | 25 phút → 10 phút | Workflow (AI parse free text) |
| #2 | So sánh giá giữa các app | Phải mở nhiều app, gõ lại tên món | 5-10 phút → <1 phút | Agent (cần crawl) |
| #3 | Xác nhận đơn với quán | Chờ reply, phải gọi điện | 5 phút → 30 giây | Workflow (template + auto-retry) |
| #4 | Dự trù giờ order sai | Không có dữ liệu thời gian thực | Lệch >15′ từ 40% → 10% | Rule (thống kê) + Workflow |
| #5 | Áp lực hỏi "đến đâu rồi?" | Người order là cầu nối thủ công | Số câu hỏi → 0 | Workflow (share link) |

---
