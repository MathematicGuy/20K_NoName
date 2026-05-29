---
# 01 — Individual Problem Scan (cá nhân)

## Scan rộng (5 problems trọng tâm)

Tôi chọn 5 problems từ trải nghiệm thực tế khi order đồ ăn trưa cho nhóm văn phòng (5-10 người). Các problem này đều có **workflow lặp lại hàng ngày**, **tốn thời gian rõ ràng**, và **có thể đo lường**.

| # | Lăng kính | Problem quan sát được | Ai đang đau? | Dấu hiệu thật |
|---|---|---|---|---|
| 1 | Lặp lại + Tốn thời gian | Tổng hợp đơn hàng từ tin nhắn rải rác (text, ảnh, nút bấm lộn xộn) trong group chat | HR/Admin (người order) | Mỗi ngày mất 30-45 phút để lội ngược chat, copy-paste vào Excel, dễ sót đơn |
| 2 | Lặp lại + Pain từ người khác | Mọi người đổi món, thêm món, hủy món vào phút chót, HR phải cập nhật liên tục | HR/Admin | Tin nhắn "cho em đổi sang cơm gà", "thêm trà đào" xuất hiện sau 11h, gây loạn |
| 3 | Tốn thời gian + AI có thể tốt hơn | Chia tiền và thu tiền: tự tính ship, giảm giá, tiền lẻ, sau đó đối chiếu chuyển khoản thủ công | HR/Admin, kế toán | Mỗi bữa mất 15-20 phút bấm máy tính + check ngân hàng; hay bị thiếu tiền do ai đó quên |
| 4 | Pain từ người khác | Nhân viên quên đặt hoặc quên trả tiền, HR phải nhắc nhở lặp lại, dễ sinh căng thẳng | HR/Admin, cả team | HR nhắn "bạn A ơi chưa chuyển tiền", nhân viên cảm thấy bị soi |
| 5 | Lặp lại + Tốn thời gian | Nhập menu từ ảnh/link quán mới vào hệ thống (hoặc vào chat) một cách thủ công | HR/Admin | Khi đổi quán, HR mất 10-15 phút gõ lại từng món + giá |

---

## Problem Card #1 — Tổng hợp đơn hàng từ chat rải rác

**Problem 1 câu:**  
Mỗi ngày, người phụ trách (HR/Admin) mất 30-45 phút để lướt ngược group chat, tổng hợp các yêu cầu đặt món (text, ảnh, nút bấm) vào Excel, dễ bị sót hoặc nhầm đơn.

**Actor:**  
HR/Admin (hoặc người luân phiên order).

**Thời điểm / bối cảnh:**  
Khung 10h30 – 11h30 hàng ngày, khi nhân viên gửi đơn rải rác.

**Current workflow:**

```text
1. HR gửi menu (ảnh/link) vào group chat lúc 10h00
2. Nhân viên reply bằng nhiều dạng: "cơm sườn", "em ơi cho chị gà rán", bấm nút (nếu có), gửi ảnh món...
3. HR liên tục mở chat, đọc từng tin, copy tên món + tên người vào Excel (30-45 phút tích tụ)
4. Đến 11h30, HR phải dò lại xem ai chưa đặt, lại nhắn hỏi
5. Sau khi chốt, HR gõ lại danh sách từ Excel sang app đặt đồ (Grab/Zalo)
```

**Bottleneck:**  
Bước 3 – đọc và nhập thủ công từ chat đa dạng format. Không có cấu trúc thống nhất.

**Impact:**  
30-45 phút/ngày × 5 ngày = 150-225 phút/tuần. Dễ sót đơn (5-10% sai sót), nhân viên phàn nàn.

**Success metric:**  
Giảm thời gian tổng hợp xuống dưới 5 phút/ngày, tỷ lệ sót đơn = 0%.

**Non-AI alternative:**  
Dùng Google Form hoặc Typeform để thu thập đơn. Nhưng nhân viên ngại mở link, tỷ lệ phản hồi thấp hơn chat.

**AI hypothesis:**  
AI đọc tin nhắn tự do (text, emoji, viết tắt), trích xuất (người, món, số lượng, yêu cầu đặc biệt), tự động tổng hợp thành bảng.

**Quick gut:**  
Workflow.

### Draft current workflow

```text
CURRENT STATE — 40 phút

[1 Gửi menu: 2']
→ [2 Nhân viên reply rải rác: 20'] (không phải effort của HR, nhưng kéo dài)
→ [3 HR lội chat + nhập Excel: 25']  <-- bottleneck
→ [4 HR hỏi người chưa đặt: 5']
→ [5 HR nhập lại lên app đặt món: 8']
```

### Draft future workflow

```text
FUTURE STATE — 8 phút

[1 Bot tự gửi menu dạng interactive: 0']
→ [2 Nhân viên chọn món (nút bấm hoặc nhắn tự do): 5']
→ [3 AI parse + tổng hợp real-time: 0']
→ [4 AI tự nhắc người chưa đặt: 0']
→ [5 HR kiểm tra bảng tổng hợp (1 click): 2']
→ [6 HR copy danh sách đã format vào app đặt hàng: 1']

Fallback: AI parse sai 1-2 món → HR sửa trực tiếp trên bảng.
```

---

## Problem Card #2 — Xử lý đổi món / thêm món phút chót

**Problem 1 câu:**  
Nhân viên thường xuyên đổi ý, thêm món hoặc hủy món sau khi đã gửi đơn, khiến HR phải cập nhật thủ công nhiều lần, dễ rối loạn dữ liệu.

**Actor:**  
HR/Admin + nhân viên.

**Thời điểm / bối cảnh:**  
Từ lúc nhân viên gửi đơn đầu tiên đến trước khi chốt (thường 11h30).

**Current workflow:**

```text
1. Nhân viên A gửi "cơm tấm" lúc 10h15
2. 10h45, A nhắn "đổi sang bún bò giúp em"
3. HR phải tìm dòng của A trong Excel, sửa thủ công
4. Nếu A hủy luôn, HR xóa dòng
5. Nhiều người đổi cùng lúc → Excel loạn, HR dễ bấm nhầm
```

**Bottleneck:**  
Việc cập nhật thủ công không theo kịp tốc độ thay đổi, đặc biệt khi group lớn (>10 người).

**Impact:**  
Mỗi lần đổi mất 2-3 phút, mỗi ngày 3-5 lần → 6-15 phút. Tỷ lệ sai sót tăng lên 10-15%.

**Success metric:**  
HR không cần can thiệp khi nhân viên đổi món; hệ thống tự cập nhật.

**Non-AI alternative:**  
Dùng bảng tính shared (Google Sheets) để nhân viên tự sửa. Nhưng họ sợ phá hỏng công thức hoặc xóa nhầm.

**AI hypothesis:**  
AI hiểu yêu cầu "đổi món", "thêm", "hủy" từ tin nhắn, tự động cập nhật đơn hàng tương ứng với đúng người.

**Quick gut:**  
Workflow (mở rộng từ problem #1).

---

## Problem Card #3 — Chia tiền, thu tiền và đối chiếu

**Problem 1 câu:**  
Sau khi nhận đồ, HR mất 15-20 phút để tính tiền ship, áp giảm giá, chia tiền lẻ cho từng người, sau đó nhắn báo và đối chiếu chuyển khoản thủ công, dễ sai và thất thoát.

**Actor:**  
HR/Admin.

**Thời điểm / bối cảnh:**  
Sau khi đồ ăn được giao (khoảng 12h-12h30).

**Current workflow:**

```text
1. HR nhận hóa đơn tổng (có ship, giảm giá)
2. HR tính tổng tiền mỗi người: (giá món + (ship/số người) - giảm giá)
3. HR gửi bảng số tiền + QR code vào group (hoặc nhắn riêng)
4. Nhân viên chuyển khoản, ghi nội dung (hoặc không)
5. HR mở app ngân hàng, kiểm tra từng giao dịch, đối chiếu với danh sách
6. Nếu ai chưa chuyển, HR nhắc lại (có thể nhiều lần)
```

**Bottleneck:**  
Bước 2 (tính toán thủ công) và bước 5 (đối chiếu chuyển khoản) tốn nhiều thời gian, dễ nhầm số lẻ.

**Impact:**  
15-20 phút/ngày, thất thoát trung bình 2-3% do tính sai hoặc người quên trả.

**Success metric:**  
HR chỉ mất 1 phút để xác nhận; tiền được tự động đối chiếu; không còn nợ quá hạn.

**Non-AI alternative:**  
Dùng app tách bill (Splitwise) nhưng nhân viên phải cài thêm app, không tích hợp sẵn với chat.

**AI hypothesis:**  
AI đọc hóa đơn (ảnh chụp), tự tính tiền cho từng người dựa trên đơn hàng đã ghi nhận, tự động gửi QR động kèm số tiền chính xác, kết nối webhook ngân hàng để tự gạch nợ.

**Quick gut:**  
Workflow + Agent nhẹ (tích hợp API thanh toán).

---

## Problem Card #4 — Nhắc nhở người quên đặt / quên trả tiền

**Problem 1 câu:**  
HR phải thủ công nhắn tin nhắc nhở từng người chưa đặt món trước giờ chốt, và nhắc những người chưa thanh toán sau bữa ăn, gây mất thời gian và tạo cảm giác khó chịu.

**Actor:**  
HR/Admin, nhân viên.

**Thời điểm / bối cảnh:**  
Lần 1: 10h45-11h15 (trước chốt), lần 2: 13h-14h (sau ăn).

**Current workflow:**

```text
1. HR nhìn danh sách đã đặt, xác định ai chưa thấy tên
2. HR @từng người hoặc nhắn riêng: "bạn đặt món chưa?"
3. Mỗi lần nhắc tốn 1-2 phút x 3-5 người = 5-10 phút
4. Sau ăn, HR soát lại ai chưa chuyển khoản, lại nhắn riêng từng người
5. Có người nhắc 2-3 lần mới trả, HR phải theo dõi nhiều ngày
```

**Bottleneck:**  
HR làm việc thủ công, dễ bỏ sót ai đó, và việc nhắc nhở có thể gây căng thẳng giao tiếp.

**Impact:**  
Mỗi ngày 10-15 phút cho việc nhắc, plus rủi ro ức chế tinh thần.

**Success metric:**  
HR không cần nhắc thủ công; hệ thống tự nhắc thông minh (vui vẻ, không làm phiền quá mức).

**Non-AI alternative:**  
Lên lịch nhắc cố định (VD: 11h bot gửi "Ai chưa đặt ơi") nhưng dễ bị lờ, không phân biệt được ai thực sự chưa đặt.

**AI hypothesis:**  
AI biết danh sách đã đặt, tự động nhắn riêng (DM) cho người chưa đặt/chưa thanh toán với văn phong đa dạng, có thể tag trực tiếp, và không làm phiền người đã hoàn thành.

**Quick gut:**  
Workflow (rule-based reminder + chút AI để cá nhân hóa nội dung).

---

## Problem Card #5 — Nhập menu từ ảnh / link quán mới

**Problem 1 câu:**  
Khi muốn đổi quán, HR mất 10-15 phút để gõ lại toàn bộ tên món và giá từ ảnh chụp menu hoặc từ link web vào hệ thống chat hoặc bảng tính.

**Actor:**  
HR/Admin.

**Thời điểm / bối cảnh:**  
Khi cần thay đổi nhà cung cấp (khoảng 1-2 lần/tuần).

**Current workflow:**

```text
1. HR tìm quán mới trên Grab/ShopeeFood/Zalo
2. Chụp ảnh menu hoặc copy link
3. HR gõ tay từng món và giá vào Excel hoặc vào tin nhắn group
4. Kiểm tra lại cho khớp, có khi gõ sai giá
```

**Bottleneck:**  
Nhập tay hoàn toàn, dễ sai và mất thời gian.

**Impact:**  
Mỗi lần đổi quán mất 10-15 phút, nếu đổi 2 lần/tuần → 20-30 phút.

**Success metric:**  
HR chỉ cần gửi ảnh hoặc link, menu tự được trích xuất và hiển thị dạng chọn món trong vòng 30 giây.

**Non-AI alternative:**  
Yêu cầu quán gửi file Excel, nhưng quán nhỏ thường không có.

**AI hypothesis:**  
AI OCR đọc ảnh menu (hoặc crawl link web), tự động nhận diện tên món, giá, nhóm món (món chính, đồ uống, topping) và tạo giao diện tương tác.

**Quick gut:**  
Workflow + AI (Computer Vision / OCR).

---

## Tổng hợp 5 Problem Cards

| Card | Problem chính | Bottleneck chính | Success metric | Quick gut |
|---|---|---|---|---|
| #1 | Tổng hợp đơn từ chat rải rác | Nhập tay từ nhiều format | 40' → <8', 0% sót | Workflow (AI parse) |
| #2 | Đổi món / thêm môn phút chót | Cập nhật thủ công liên tục | HR không cần can thiệp | Workflow mở rộng |
| #3 | Chia tiền, thu tiền, đối chiếu | Tính toán + check ngân hàng | 20' → 1', tự động | Workflow + Agent |
| #4 | Nhắc nhở quên đặt/quên trả | HR phải @từng người | 0 lần HR nhắc | Workflow (rule + AI nội dung) |
| #5 | Nhập menu từ ảnh/link | Gõ tay tên món, giá | 15' → 30 giây | Workflow + OCR |

---
