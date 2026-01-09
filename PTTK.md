## 1. Yêu cầu về hiệu năng (Performance)

* Thời gian tải trang:
  * Trang chủ, trang danh mục: ≤ **3 giây**
  * Trang chi tiết sản phẩm: ≤ **2 giây**
* Khả năng xử lý:
  * Hỗ trợ tối thiểu **1.000–5.000 người dùng đồng thời**
  * Xử lý nhanh các thao tác tìm kiếm, lọc sản phẩm, thêm vào giỏ hàng
* Tối ưu:
  * Sử dụng cache cho sản phẩm phổ biến
  * Tối ưu hình ảnh

---

## 2. Yêu cầu về khả năng mở rộng (Scalability)

* Hệ thống có thể mở rộng:
  * Khi số lượng sản phẩm tăng (10.000+ sản phẩm)
  * Khi lượng truy cập tăng cao vào các dịp khuyến mãi
* Hỗ trợ mở rộng theo chiều:
  * Nâng cấp server
  * Tách dịch vụ (database, payment, search)

---

## 3. Yêu cầu về bảo mật (Security)

* Xác thực và phân quyền:

  * Người dùng, quản trị viên, nhân viên
* Bảo mật dữ liệu:

  * Mã hóa mật khẩu
  * HTTPS cho toàn bộ website
* Thanh toán:

  * Tuân thủ chuẩn bảo mật thanh toán (PCI-DSS nếu có)

---

## 4. Yêu cầu về độ tin cậy & tính sẵn sàng (Reliability & Availability)

* Tính sẵn sàng:

  * Website hoạt động **99.5% – 99.9% uptime**
* Sao lưu dữ liệu:

  * Backup hàng ngày (database, đơn hàng)

---

## 5. Yêu cầu về khả năng sử dụng (Usability)

* Giao diện:
  * Thân thiện, dễ sử dụng cho người không rành công nghệ
  * Phù hợp cho mọi độ tuổi
* Tìm kiếm & điều hướng:
  * Dễ tìm sản phẩm theo hãng, giá, cấu hình
* Responsive:
  * Hoạt động tốt trên **desktop**
* Hỗ trợ:
  * Thông báo lỗi rõ ràng
  * Hướng dẫn đặt hàng, thanh toán

---

## 6. Yêu cầu về khả năng tương thích (Compatibility)

* Trình duyệt:
  * Chrome, Firefox, Edge, Safari
* Thiết bị:
  * PC, laptop
* Tích hợp:
  * Cổng thanh toán (VNPay, MoMo, ZaloPay…)
  * Đơn vị vận chuyển

---

## 7. Yêu cầu về khả năng bảo trì (Maintainability)

* Mã nguồn:

  * Dễ đọc, có tài liệu
* Dễ cập nhật:

  * Thêm sản phẩm, thay đổi giá, khuyến mãi không ảnh hưởng hệ thống

---

## 8. Yêu cầu về pháp lý & tuân thủ (Legal & Compliance)

* Tuân thủ:

  * Luật bảo vệ dữ liệu cá nhân
  * Chính sách bảo mật và điều khoản sử dụng
* Lưu trữ thông tin khách hàng
