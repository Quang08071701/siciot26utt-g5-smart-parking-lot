# Smart Parking IoT System

## 1. Vấn đề xảy ra ở đâu?

Vấn đề xảy ra tại **khu vực bãi đỗ xe**, đặc biệt là lối vào, lối ra và khu vực quản lý số lượng chỗ đỗ.

Bãi có **10 chỗ đỗ xe**, nhưng người lái xe không biết chính xác còn bao nhiêu chỗ trống trước khi đi vào. Đồng thời, việc quản lý xe vào/ra và xác định xe nào đã vào bãi còn thực hiện thủ công.

---

## 2. Ai gặp vấn đề?

### 👨‍💼 Người lái xe

* Khó biết bãi còn chỗ hay đã đầy.
* Có thể phải đi vào bãi mới biết còn chỗ trống.
* Mất thời gian khi bãi đã đầy.

### Nhân viên bảo vệ / quản lý bãi

* Phải theo dõi xe vào và xe ra.
* Phải kiểm tra số lượng chỗ còn trống.
* Có thể phải đếm xe bằng mắt hoặc ghi chép thủ công.

### Chủ bãi xe

* Khó kiểm soát tình trạng sử dụng bãi.
* Khó theo dõi số lượng xe vào/ra.
* Khó quản lý và thống kê lượt xe.

---

## 3. Khi nào vấn đề xảy ra?

Vấn đề đặc biệt xảy ra trong các trường hợp:

* Có nhiều xe vào/ra cùng lúc.
* Giờ cao điểm, lượng xe tăng cao.
* Người lái xe không biết trước bãi còn chỗ hay không.
* Nhân viên phải liên tục đếm xe bằng mắt.
* Việc ghi chép xe vào/ra được thực hiện thủ công.

---

## 4. Hiện tại họ xử lý bằng cách nào?

Một số bãi xe có thể sử dụng các phương pháp:

* Nhân viên quan sát và đếm xe thủ công.
* Dùng vé giấy hoặc thẻ để kiểm soát xe.
* Ghi chép thông tin xe vào/ra.
* Sử dụng bảng thông báo số chỗ trống nhưng cần cập nhật thủ công.

Các phương pháp này có thể hoạt động với bãi nhỏ, nhưng khi số lượng xe tăng thì việc quản lý trở nên khó khăn và dễ xảy ra sai sót.

---

## 5. Điểm bất tiện, rủi ro hoặc tốn kém là gì?

### Bất tiện

* Người lái xe phải vào bãi mới biết còn chỗ hay không.
* Nhân viên phải liên tục theo dõi tình trạng bãi.
* Dễ mất thời gian khi lượng xe vào/ra đông.
* Việc quản lý thủ công gây khó khăn khi cần thống kê.

### Rủi ro

* Có thể đếm sai số lượng xe.
* LED có thể hiển thị sai số chỗ trống.
* Có thể xảy ra tình trạng hệ thống báo còn chỗ nhưng thực tế bãi đã đầy.
* Vé hoặc thông tin xe được quản lý thủ công có thể bị thất lạc hoặc nhầm lẫn.

### Tốn kém

* Cần nhân viên trực để theo dõi và quản lý.
* Chi phí nhân sự tăng khi quy mô bãi lớn.
* Nếu xây dựng hệ thống lớn sử dụng camera AI thì chi phí thiết bị, triển khai và xử lý dữ liệu có thể cao.

---

## 6. Giải pháp đề xuất

Xây dựng **Smart Parking IoT System** nhằm tự động hóa việc theo dõi và quản lý bãi đỗ xe.

Hệ thống sử dụng cảm biến để phát hiện xe vào/ra và tự động cập nhật số lượng chỗ trống.

### Chức năng chính

* Phát hiện xe vào/ra.
* Đếm số lượng xe trong bãi.
* Theo dõi số chỗ trống.
* Hiển thị số chỗ còn trống bằng LED.
* Cảnh báo khi bãi đầy.
* Theo dõi dữ liệu trên Dashboard.
* Có thể mở rộng điều khiển và giám sát từ điện thoại.
* Tự động cập nhật trạng thái bãi xe.

---

## 7. Mục tiêu của hệ thống

Hệ thống hướng tới việc:

> **Tự động phát hiện xe → cập nhật số lượng xe → tính số chỗ trống → hiển thị trạng thái bãi xe → cảnh báo khi bãi đầy.**

Qua đó giúp giảm việc quản lý thủ công, giảm sai sót và giúp người lái xe biết được tình trạng bãi đỗ một cách nhanh chóng.

---

## 8. Quy mô hệ thống

Bãi đỗ xe trong mô hình có:

* **Tổng số chỗ:** 10
* **Số xe hiện tại:** được cập nhật tự động
* **Số chỗ trống:** `10 - số xe hiện tại`

Ví dụ:

| Số xe | Chỗ trống | Trạng thái       |
| ----: | --------: | ---------------- |
|     0 |        10 | 🟢 Còn nhiều chỗ |
|     3 |         7 | 🟢 Còn chỗ       |
|     7 |         3 | 🟡 Gần đầy       |
|     9 |         1 | 🟠 Sắp đầy       |
|    10 |         0 | 🔴 Bãi đầy       |

---

## 9. Kết quả mong muốn

Sau khi triển khai, hệ thống có thể:

* Tự động cập nhật số lượng xe.
* Hiển thị chính xác số chỗ trống.
* Giảm sự phụ thuộc vào việc đếm xe thủ công.
* Giúp nhân viên dễ dàng theo dõi tình trạng bãi.
* Giúp người lái xe nhanh chóng biết bãi còn chỗ hay không.
* Tạo nền tảng để mở rộng thành hệ thống quản lý bãi đỗ xe thông minh.

---

## 10. Hướng phát triển

Trong tương lai, hệ thống có thể mở rộng thêm:

* Nhận diện biển số xe bằng camera.
* Ứng dụng mobile cho người dùng.
* Giám sát bãi xe từ xa qua Internet.
* Lưu trữ dữ liệu trên Cloud.
* Thống kê lượt xe theo ngày/tháng.
* Tích hợp thanh toán phí gửi xe.
* AI phân tích tình trạng sử dụng bãi.
