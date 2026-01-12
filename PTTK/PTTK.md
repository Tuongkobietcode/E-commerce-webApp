# Tài liệu phân tích thiết kế hệ thống High Tech Shop



**1. Giới thiệu dự án**

Dự án “ *Web bán thiết bị điện tử công nghệ* ” là một hệ thống thương mại điện tử cho phép khách hàng xem – chọn – mua các sản phẩm công nghệ như Laptop, PC, Smartphone, Tablet, Phụ kiện…

Hệ thống được chia thành hai phần chính:

* **Client Website:** dành cho khách hàng mua sắm
* **Admin Dashboard:** dành cho ban quản lý cửa hàng

Website hướng đến trải nghiệm mua sắm hiện đại, tốc độ cao, dễ sử dụng và tối ưu trên nhiều thiết bị.


2.Công nghệ sử dụng

3.Các tác nhân tham gia 

4.Yêu cầu chức năng

5.Yêu cầu phi chức năng

6.Các use  case

7.Kịch bản use case


### **UC01 – Đăng ký tài khoản**

**Mô tả**

Khách hàng tạo tài khoản mới để sử dụng hệ thống.

**Actor**

* Khách hàng

**Tiền điều kiện**

* Người dùng chưa có tài khoản.

**Hậu điều kiện**

* Tài khoản được tạo và lưu vào hệ thống.

**Dòng sự kiện chính**

1. Người dùng chọn chức năng “Đăng ký”.
2. Nhập thông tin: email, họ tên, mật khẩu, số điện thoại.
3. Hệ thống kiểm tra thông tin hợp lệ.
4. Hệ thống gửi mã OTP (nếu có).
5. Người dùng nhập mã OTP.
6. Hệ thống tạo tài khoản và thông báo thành công.

**Ngoại lệ**

* Email đã tồn tại → thông báo lỗi.
* Mã OTP sai hoặc hết hạn → yêu cầu nhập lại.

## **UC02 – Đăng nhập**

**Mô tả**

Người dùng đăng nhập vào hệ thống.

**Actor**

* Khách hàng
* Admin

**Tiền điều kiện**

* Tài khoản đã tồn tại và kích hoạt.

**Hậu điều kiện**

* Hệ thống tạo phiên đăng nhập (JWT Token).

**Dòng sự kiện chính**

1. Người dùng nhập email/mật khẩu.
2. Hệ thống kiểm tra thông tin.
3. Đăng nhập thành công và chuyển đến trang chủ.

**Ngoại lệ**

* Sai email/mật khẩu → thông báo lỗi.
* Tài khoản bị khóa → từ chối truy cập.

### **UC03 – Tìm kiếm & xem sản phẩm**

**Mô tả**

Khách hàng tìm kiếm và xem chi tiết sản phẩm.

**Actor**

* Khách hàng

**Tiền điều kiện**

* Sản phẩm phải tồn tại trong hệ thống.

**Hậu điều kiện**

* Hiển thị danh sách hoặc thông tin chi tiết sản phẩm.

**Dòng sự kiện chính**

1. Người dùng nhập từ khóa vào ô tìm kiếm.
2. Hệ thống hiển thị kết quả tương ứng.
3. Người dùng chọn 1 sản phẩm.
4. Hệ thống hiển thị thông tin chi tiết:
   * Giá, hình ảnh, cấu hình
   * Tồn kho theo biến thể
   * Đánh giá và bình luận

**Ngoại lệ**

* Không tìm thấy sản phẩm → báo “Không có kết quả”.

### **UC04 – So sánh sản phẩm**

**Mô tả**

Khách hàng so sánh thông số kỹ thuật của nhiều sản phẩm.

**Actor**

* Khách hàng

**Tiền điều kiện**

* Có ít nhất 2 sản phẩm hợp lệ được chọn.

**Hậu điều kiện**

* Hiển thị bảng so sánh.

**Dòng sự kiện chính**

1. Người dùng chọn sản phẩm A → nhấn “So sánh”.
2. Hệ thống yêu cầu chọn thêm sản phẩm B.
3. Người dùng chọn sản phẩm B.
4. Hệ thống hiển thị bảng so sánh:
   * Cấu hình, giá, ưu/nhược điểm, tình trạng kho.

**Ngoại lệ**

* Chọn sản phẩm không cùng danh mục → báo không thể so sánh.

### **UC05 – Thêm vào giỏ hàng**

**Mô tả**

Khách hàng thêm sản phẩm đã chọn vào giỏ.

**Actor**

* Khách hàng

**Tiền điều kiện**

* Sản phẩm còn hàng.

**Hậu điều kiện**

* Sản phẩm được thêm vào giỏ hàng.

**Dòng sự kiện chính**

1. Khách hàng chọn sản phẩm.
2. Chọn biến thể (màu sắc/dung lượng).
3. Nhấn “Thêm vào giỏ”.
4. Hệ thống kiểm tra tồn kho biến thể.
5. Thêm sản phẩm vào giỏ và thông báo thành công.

**Ngoại lệ**

* Hết hàng → báo hết hàng.

### **UC06 – Mua hàng**

**Mô tả**

Khách hàng tiến hành đặt hàng online.

**Actor**

* Khách hàng

**Tiền điều kiện**

* Giỏ hàng không trống.
* Người dùng đã đăng nhập.

**Hậu điều kiện**

* Đơn hàng được tạo và chờ xác nhận.

**Dòng sự kiện chính**

1. Người dùng vào giỏ hàng và chọn “Thanh toán”.
2. Chọn địa chỉ giao hàng.
3. Chọn phương thức thanh toán (COD/VNPay/MoMo).
4. Hệ thống tính tổng tiền + phí ship.
5. Người dùng xác nhận đơn.
6. Hệ thống tạo đơn hàng và thông báo thành công.

**Ngoại lệ**

* Không đủ hàng → thông báo cập nhật giỏ.
* Thanh toán online thất bại → báo lỗi.

### **UC07 – Theo dõi đơn hàng**

**Mô tả**

Khách hàng xem tình trạng đơn hàng của mình.

**Actor**

* Khách hàng

**Tiền điều kiện**

* Đơn hàng đã được tạo.

**Hậu điều kiện**

* Hiển thị trạng thái mới nhất của đơn.

**Dòng sự kiện chính**

1. Người dùng mở trang “Đơn hàng của tôi”.
2. Chọn 1 đơn hàng.
3. Hệ thống hiển thị trạng thái:
   * Chờ xác nhận → Đóng gói → Giao hàng → Thành công
4. Hiển thị thông tin vận chuyển realtime.

**Ngoại lệ**

* Đơn đã bị hủy → hiển thị lý do.

### **UC08 – Yêu cầu đổi trả**

**Mô tả**

Khách yêu cầu đổi trả theo chính sách.

**Actor**

* Khách hàng

**Tiền điều kiện**

* Đơn đã giao thành công.
* Còn trong thời gian đổi trả.

**Hậu điều kiện**

* Yêu cầu đổi trả được gửi đến admin.

**Dòng sự kiện chính**

1. Người dùng chọn 1 đơn hàng.
2. Nhấn “Yêu cầu đổi trả”.
3. Chọn lý do đổi trả + tải ảnh đính kèm.
4. Hệ thống gửi yêu cầu tới Admin.
5. Admin kiểm tra và phản hồi.

**Ngoại lệ**

* Hết thời gian cho phép đổi trả → báo lỗi.

### **UC09 – Quản lý sản phẩm (Admin)**

**Mô tả**

Admin tạo và cập nhật sản phẩm.

**Actor**

* Admin

**Tiền điều kiện**

* Admin đã đăng nhập.

**Hậu điều kiện**

* Sản phẩm được cập nhật/hệ thống.

**Dòng sự kiện chính**

1. Admin vào trang quản lý sản phẩm.
2. Thêm/sửa/xóa sản phẩm:
   * tên, mô tả, hình ảnh
   * giá bán
   * danh mục
   * biến thể (màu/dung lượng)
   * thông số kỹ thuật
3. Hệ thống lưu dữ liệu vào DB.

**Ngoại lệ**

* Sản phẩm trùng tên/sku → báo lỗi.

### **UC10 – Quản lý kho / serial**

**Mô tả**

Quản lý nhập – xuất – tồn kho theo lô và serial.

**Actor**

* Admin
* Nhân viên kho

**Tiền điều kiện**

* Sản phẩm đã tồn tại.

**Hậu điều kiện**

* Thông tin kho được cập nhật.

**Dòng sự kiện chính**

1. Nhập kho:
   * tạo lô
   * nhập số lượng
   * nhập serial/IMEI
2. Kiểm kê kho:
   * xem tồn theo serial
   * điều chỉnh chênh lệch
3. Xuất kho:
   * khi đơn hàng được duyệt
   * chọn serial để xuất

**Ngoại lệ**

* Serial trùng → từ chối lưu.

### **UC11 – Quản lý đơn hàng (Admin)**

**Mô tả**

Admin theo dõi và xử lý đơn hàng của khách.

**Actor**

* Admin

**Tiền điều kiện**

* Đơn hàng đã tạo.

**Hậu điều kiện**

* Trạng thái đơn được cập nhật.

**Dòng sự kiện chính**

1. Admin mở danh sách đơn hàng.
2. Xác nhận đơn.
3. Gán serial cho từng sản phẩm.
4. Cập nhật trạng thái:
   * Đóng gói
   * Chờ giao
   * Đang giao
   * Thành công
5. Quản lý đổi trả và hoàn tiền.

**Ngoại lệ**

* Không còn serial phù hợp → báo lỗi.

### **UC12 – Quản lý khuyến mãi**

**Mô tả**

Tạo và quản lý các chương trình khuyến mãi.

**Actor**

* Admin
* Nhân viên marketing

**Tiền điều kiện**

* Admin đã đăng nhập.

**Hậu điều kiện**

* Khuyến mãi được kích hoạt.

**Dòng sự kiện chính**

1. Tạo chương trình khuyến mãi:
   * kiểu giảm giá (%/đ tiền)
   * theo sản phẩm/danh mục
   * thời gian áp dụng
   * giới hạn số lượng
2. Hệ thống lưu và áp dụng tự động.

**Ngoại lệ**

* Ngày bắt đầu > ngày kết thúc → báo lỗi.

### **UC13 – Quản lý khách hàng**

**Mô tả**

Admin quản lý danh sách khách hàng.

**Actor**

* Admin
* CSKH

**Tiền điều kiện**

* Tài khoản khách hàng đã tồn tại.

**Hậu điều kiện**

* Dữ liệu khách hàng được cập nhật.

**Dòng sự kiện chính**

1. Xem danh sách khách hàng.
2. Xem lịch sử mua hàng của 1 khách.
3. Khoá/Tạm khoá tài khoản.
4. Cập nhật thông tin khách hàng (nếu cần).

**Ngoại lệ**

* Khách hàng bị khoá vẫn đặt đơn → từ chối tạo đơn.
