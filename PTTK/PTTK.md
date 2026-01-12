# Tài liệu phân tích thiết kế hệ thống High Tech Shop

**1. Giới thiệu dự án**

Dự án “ _Web bán thiết bị điện tử công nghệ_ ” là một hệ thống thương mại điện tử cho phép khách hàng xem – chọn – mua các sản phẩm công nghệ như Laptop, PC, Smartphone, Tablet, Phụ kiện…

Hệ thống được chia thành hai phần chính:

- **Client Website:** dành cho khách hàng mua sắm
- **Admin Dashboard:** dành cho ban quản lý cửa hàng

Website hướng đến trải nghiệm mua sắm hiện đại, tốc độ cao, dễ sử dụng và tối ưu trên nhiều thiết bị.

2.Công nghệ sử dụng

3.Các tác nhân tham gia

Khách hàng : Người mua thiết bị điện tử trên hệ thống

Quản trị viên: Người quản lý toàn bộ hệ thống

Nhân viên bán hàng : Xử lý nghiệp vụ bán hàng

Nhân viên kho: Quản lý tồn kho

Đơn vị giao hàng: Hệ thống hoặc đối tác bên ngoài

4.Yêu cầu chức năng

5.Yêu cầu phi chức năng

6.Các use case

6.1 xác định tác nhân và usecase

các tác nhân của hệ thống:

Quản trị viên : có thể là chủ cửa hàng .Đây là người quản lý tất cả các nghiệp vụ của cửa hàng

Nhân viên kho: là người chịu trách nhiệm quản lý hàng hóa trong kho. Mỗi nhân viên kho sẽ được quản trị viên tạo một tài khoản cá nhân để thực hiện các nghiệp vụ liên quan đến kho.

Nhân viên bán hàng: là người xử lý các nghiệp vụ bán hàng .

Khách hàng : người sử dụng hệ thống để mua thiết bị điện tử.

Cổng thanh toán: là hệ thống bên ngoài có nhiệm vụ xử lý các giao dịch thanh toán cho đơn hàng.

Đơn vị giao hàng: là đối tác vận chuyển bên ngoài , chịu trách nhiệm vận chuyển thiết bị điện tử đến khách hàng .

Khách vãng lai: là người truy cập hệ thống nhưng chưa đăng ký hoặc chưa đăng nhập tài khoản . Họ chỉ có thể sử dụng các chức năng cơ bản của hệ thống.

Danh sách tác nhân và use case:

| STT | Tên tác nhân        | Use case                                                                                           |
| --- | ------------------- | -------------------------------------------------------------------------------------------------- |
| 1   | Quản trị viên       | Quản lý khách hàng, quản lý đơn hàng, quản lý sản phẩm, quản lý khuyến mãi,đăng nhập               |
| 2   | Khách hàng          | Đăng nhập, Thanh toán, quản lý giỏ hàng, đặt hàng,đăng ký tài khoản,tìm kiếm sản phẩm,xem sản phẩm |
| 3   | Khách hàng vãng lai | tìm kiếm sản phẩm, xem sản phẩm                                                                    |
| 4   | Nhân viên kho       | Quản lý kho, đăng nhập                                                                             |
