# Tài liệu phân tích thiết kế hệ thống High Tech Shop

**1. Giới thiệu dự án**

Dự án “ _Web bán thiết bị điện tử công nghệ_ ” là một hệ thống thương mại điện tử cho phép khách hàng xem – chọn – mua các sản phẩm công nghệ như Laptop, PC, Smartphone, Tablet, Phụ kiện…

Hệ thống được chia thành hai phần chính:

- **Client Website:** dành cho khách hàng mua sắm
- **Admin Dashboard:** dành cho ban quản lý cửa hàng

Website hướng đến trải nghiệm mua sắm hiện đại, tốc độ cao, dễ sử dụng và tối ưu trên nhiều thiết bị.

2.Công nghệ sử dụng

3.Các tác nhân tham gia

### 4. Yêu cầu chức năng

#### 4.1. Quản lý người dùng

- Đăng ký tài khoản
- Đăng nhập / đăng xuất
- Quên mật khẩu
- Phân quyền người dùng (Admin, Nhân viên, Khách hàng)
- Cập nhật thông tin cá nhân

---

#### 4.2 Quản lý sản phẩm

- Thêm / sửa / xóa sản phẩm
- Quản lý danh mục thiết bị điện tử

  (Ví dụ: Điện thoại, Laptop, TV, Phụ kiện…)

- Quản lý thông tin sản phẩm:

  - Tên, mô tả, hình ảnh
  - Giá bán, giá khuyến mãi
  - Thông số kỹ thuật
  - Thương hiệu, bảo hành

- Tìm kiếm và lọc sản phẩm theo:

  - Giá, thương hiệu, loại sản phẩm
  - Thông số kỹ thuật

---

#### 4.3. Quản lý kho hàng

- Theo dõi số lượng tồn kho
- Cập nhật nhập/xuất kho
- Cảnh báo khi hàng sắp hết
- Quản lý nhiều kho (nếu có)

---

#### 4.4. Chức năng mua hàng (Khách hàng)

- Xem danh sách sản phẩm
- Xem chi tiết sản phẩm
- Thêm sản phẩm vào giỏ hàng
- Cập nhật số lượng / xóa sản phẩm trong giỏ
- Đặt hàng
- Nhập thông tin giao hàng
- Áp dụng mã giảm giá / khuyến mãi

---

#### 4.5. Quản lý đơn hàng

- Tạo đơn hàng
- Cập nhật trạng thái đơn hàng:
  - Chờ xác nhận
  - Đang xử lý
  - Đang giao
  - Hoàn thành
  - Hủy đơn
- Xem lịch sử đơn hàng (khách hàng)
- Nhân viên xử lý và xác nhận đơn

---

#### 4.6. Thanh toán

- Thanh toán khi nhận hàng (COD)
- Thanh toán online:
  - Ví điện tử
  - Thẻ ngân hàng
- Ghi nhận trạng thái thanh toán
- Xử lý hoàn tiền (nếu có)

---

#### 4.7. Vận chuyển

- Tính phí vận chuyển
- Kết nối đơn vị giao hàng
- Theo dõi trạng thái giao hàng
- Cập nhật mã vận đơn

---

#### 4.8. Khuyến mãi & ưu đãi

- Quản lý mã giảm giá
- Chương trình khuyến mãi theo sản phẩm/danh mục
- Flash sale
- Giới hạn số lần sử dụng mã

---

#### 4.9. Đánh giá & phản hồi

- Khách hàng đánh giá sản phẩm
- Bình luận, xếp hạng sao
- Quản trị viên duyệt/xóa đánh giá không phù hợp

---

#### 4.10. Báo cáo & thống kê (Admin)

- Thống kê doanh thu theo ngày/tháng/năm
- Thống kê sản phẩm bán chạy
- Báo cáo tồn kho
- Thống kê khách hàng
- Xuất báo cáo (Excel/PDF)

  5.Yêu cầu phi chức năng

  6.Các use case
