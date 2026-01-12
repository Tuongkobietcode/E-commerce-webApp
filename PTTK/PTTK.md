# Tài liệu phân tích thiết kế hệ thống High Tech Shop

**1. Giới thiệu dự án**

Dự án “ _Web bán thiết bị điện tử công nghệ_ ” là một hệ thống thương mại điện tử cho phép khách hàng xem – chọn – mua các sản phẩm công nghệ như Laptop, PC, Smartphone, Tablet, Phụ kiện…

Hệ thống được chia thành hai phần chính:

- **Client Website:** dành cho khách hàng mua sắm
- **Admin Dashboard:** dành cho ban quản lý cửa hàng

Website hướng đến trải nghiệm mua sắm hiện đại, tốc độ cao, dễ sử dụng và tối ưu trên nhiều thiết bị.

### 2.Công nghệ sử dụng

### 3.Các tác nhân tham gia

### 4.Yêu cầu chức năng

#### 4.1. Quản lý sản phẩm

* Thêm, sửa, xóa thông tin sản phẩm.
* Quản lý danh mục sản phẩm.

* Thêm/sửa các biến thể của sản phẩm:
* màu sắc, dung lượng, phiên bản, cấu hình.

* Quản lý thông số kỹ thuật chi tiết theo từng loại.
* Up hình sản phẩm (đa ảnh, ảnh 360°, video).

* Hiển thị đánh giá & bình luận từ khách hàng.

#### 4.2. Quản lý kho hàng

* Hệ thống kho hoạt động theo các nguyên tắc:
* Quản lý theo lô nhập:

* Theo dõi từng lô bởi:
* Mã lô

* Ngày nhập
* Nhà cung cấp

* Giá vốn theo lô
* Số lượng sản phẩm trong lô

* Quản lý theo serial/IMEI:
* Mỗi sản phẩm có trạng thái:

* Mới
* Trưng bày

* Lỗi
* Đổi trả

* Nghiệp vụ kho:
* Nhập kho.

* Xuất kho theo đơn hàng.
* Kiểm kê định kỳ.

* Điều chỉnh chênh lệch.
* Lịch sử biến động kho đầy đủ.

#### 4.3. Quản lý đơn hàng

* Đơn hàng được vận hành theo chu trình nghiệp vụ chuẩn TMĐT:
* Trạng thái đơn hàng:

* Chờ xác nhận
* Đã xác nhận

* Đang đóng gói
* Chờ giao cho vận chuyển

* Đang giao
* Giao thành công

* Giao thất bại
* Yêu cầu đổi trả

* Hoàn tiền / Từ chối yêu cầu
* Nghiệp vụ xử lý đơn:

* Kiểm tra tồn kho theo serial khi duyệt đơn.
* Gán serial sản phẩm vào đơn hàng.

* Hủy đơn (theo điều kiện):
* trước khi đóng gói

* Đổi trả hàng:
* cập nhật kho theo trạng thái khác (hàng đổi trả / hàng lỗi)

* Theo dõi trạng thái giao hàng qua API bên vận chuyển.

#### 4.4. Quản lý khách hàng

* Hồ sơ cá nhân.
* Nhiều địa chỉ giao hàng.

* Lịch sử đơn hàng.
* Đánh giá sản phẩm.

* Thông tin bảo hành & yêu cầu hỗ trợ.

#### 4.5. Quản lý khuyến mãi

* Cho phép tạo nhiều hình thức khuyến mãi:
* Loại chương trình:

* Giảm giá theo sản phẩm.
* Giảm giá theo danh mục.

* Giảm theo số tiền / %.
* Flash sale theo giờ.

* Mã giảm giá (Coupon).
* Điều kiện áp dụng:

* Đơn hàng tối thiểu.
* Số lượng có hạn.

* Khách hàng mới/khách hàng thân thiết.
* Chỉ áp dụng cho sản phẩm/danh mục cụ thể.

* Giới hạn theo thời gian.

#### 4.6. Chức năng dành cho khách hàng

* Đăng ký / đăng nhập (JWT, OAuth Google).
* Tìm kiếm nâng cao:

* lọc theo giá, thương hiệu, cấu hình, hiệu năng.
* So sánh sản phẩm.

* Giỏ hàng.
* Theo dõi đơn hàng realtime.

* Yêu thích sản phẩm.
* Yêu cầu bảo hành / đổi trả.

### 5.Yêu cầu phi chức năng

#### 5.1. Yêu cầu về hiệu năng (Performance)

1. Thời gian tải trang:
   * Trang chủ, trang danh mục: ≤ **3 giây**
   * Trang chi tiết sản phẩm: ≤ **2 giây**
1. Khả năng xử lý:
   * Hỗ trợ tối thiểu **1.000–5.000 người dùng đồng thời**
   * Xử lý nhanh các thao tác tìm kiếm, lọc sản phẩm, thêm vào giỏ hàng
1. Tối ưu:
   * Sử dụng cache cho sản phẩm phổ biến
   * Tối ưu hình ảnh

#### 5.2. Yêu cầu về khả năng mở rộng (Scalability)

1. Hệ thống có thể mở rộng:
   * Khi số lượng sản phẩm tăng (10.000+ sản phẩm)
   * Khi lượng truy cập tăng cao vào các dịp khuyến mãi
1. Hỗ trợ mở rộng theo chiều:
   * Nâng cấp server
   * Tách dịch vụ (database, payment, search)

#### 5.3. Yêu cầu về bảo mật (Security)

1. Xác thực và phân quyền:

   * Người dùng, quản trị viên, nhân viên
1. Bảo mật dữ liệu:

   * Mã hóa mật khẩu
   * HTTPS cho toàn bộ website
1. Thanh toán:

   * Tuân thủ chuẩn bảo mật thanh toán (PCI-DSS nếu có)

#### 5.4. Yêu cầu về độ tin cậy & tính sẵn sàng (Reliability & Availability)

1. Tính sẵn sàng:

   * Website hoạt động **99.5% – 99.9% uptime**
1. Sao lưu dữ liệu:

   * Backup hàng ngày (database, đơn hàng)

#### 5.5. Yêu cầu về khả năng sử dụng (Usability)

1. Giao diện:
   * Thân thiện, dễ sử dụng cho người không rành công nghệ
   * Phù hợp cho mọi độ tuổi
2. Tìm kiếm & điều hướng:
   * Dễ tìm sản phẩm theo hãng, giá, cấu hình
3. Responsive:
   * Hoạt động tốt trên **mọi loại màn hình**
4. xHỗ trợ:
   * Thông báo lỗi rõ ràng
   * Hướng dẫn đặt hàng, thanh toán

#### 5.6. Yêu cầu về khả năng tương thích (Compatibility)

1. Trình duyệt:
   * Chrome, Firefox, Edge, Safari
1. Thiết bị:
   * PC, laptop
1. Tích hợp:
   * Cổng thanh toán (VNPay, MoMo, ZaloPay…)
   * Đơn vị vận chuyển

#### 5.7. Yêu cầu về khả năng bảo trì (Maintainability)

1. Mã nguồn:

   * Dễ đọc, có tài liệu
1. Dễ cập nhật:

   * Thêm sản phẩm, thay đổi giá, khuyến mãi không ảnh hưởng hệ thống

#### 5.8. Yêu cầu về pháp lý & tuân thủ (Legal & Compliance)

1. Tuân thủ:

   * Luật bảo vệ dữ liệu cá nhân
   * Chính sách bảo mật và điều khoản sử dụng
1. Lưu trữ thông tin khách hàng

### 6.Các use  case
