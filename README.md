# Website bán đồ thể thao

Website thương mại điện tử bán đồ thể thao viết bằng PHP thuần và MySQL. Có giỏ hàng, đặt hàng, thanh toán, tài khoản khách hàng và mục tin tức thể thao.

## Tính năng

- Xem danh sách sản phẩm, chi tiết sản phẩm, sản phẩm tương tự, tìm kiếm.
- Giỏ hàng, kiểm tra hàng, thanh toán (có tùy chọn ví MoMo).
- Đăng ký, đăng nhập, đăng xuất, đổi mật khẩu, cập nhật hồ sơ khách hàng.
- Xem đơn hàng của tôi, chi tiết đơn, hủy đơn.
- Bình luận sản phẩm, gửi liên hệ/phản hồi.
- Tin tức thể thao, danh mục tin, câu lạc bộ và giải đấu.
- Banner trượt (slide), thống kê người đang online.

## Công nghệ

- PHP (kết nối MySQL bằng PDO và mysqli)
- MySQL / MariaDB
- HTML, CSS

## Cấu trúc chính

| File | Vai trò |
|---|---|
| `index.php` | Trang chủ |
| `dssanpham.php`, `view_chitietsp.php`, `sptuongtu.php`, `timkiem.php` | Sản phẩm và tìm kiếm |
| `cart.php`, `xyly_giohang.php`, `add.php`, `kiemtrahang.php` | Giỏ hàng |
| `thanhtoan.php`, `callback.php`, `chuyendoitien.php` | Thanh toán |
| `dangky.php`, `loginform.php`, `xuly_login.php`, `xuly_signup.php`, `logout.php` | Tài khoản |
| `hosokhachhang.php`, `updatehosokh.php`, `doimatkhau.php`, `xuly_doimatkhau.php` | Hồ sơ khách hàng |
| `donhangcuatoi.php`, `chitietdhkh.php`, `xuly_huydonhang.php` | Đơn hàng |
| `tintucthethao.php`, `view_chitiettintuc.php` | Tin tức |
| `view_gioithieu.php`, `view_lienhe.php`, `xuly_lienhe.php`, `xuly_comment.php` | Giới thiệu, liên hệ, bình luận |
| `config.php`, `dbcontroller.php` | Kết nối cơ sở dữ liệu |
| `shopthethao.sql` | Cấu trúc và dữ liệu mẫu của database |

## Cài đặt

Yêu cầu: PHP 7.4+, MySQL/MariaDB, và một web server cục bộ như XAMPP hoặc Laragon.

1. Chép mã nguồn vào thư mục web (ví dụ `htdocs/website-ban-do-the-thao`).
2. Tạo database `shopthethao` và nhập file `shopthethao.sql` (qua phpMyAdmin hoặc `mysql -u root shopthethao < shopthethao.sql`).
3. Kiểm tra thông tin kết nối trong `config.php` và `dbcontroller.php` (mặc định: host `localhost`, user `root`, database `shopthethao`) rồi sửa cho khớp máy của bạn.
4. Mở `http://localhost/website-ban-do-the-thao/`.

## Lưu ý

Dự án phục vụ học tập. Trước khi đưa lên môi trường thật, nên đổi tài khoản database mặc định, rà soát việc chống SQL injection và băm mật khẩu.
