Câu A1
1.type="range" → thanh trượt (slider) để chọn giá trị trong khoảng cho trước → dùng cho bộ lọc tìm kiếm sản phẩm theo khoảng giá.
2.type="hidden" → trường ẩn không hiển thị trên giao diện người dùng → dùng để truyền các dữ liệu nền như ID sản phẩm lên server.
3.type="radio" → nút chọn tròn, chỉ cho phép chọn duy nhất 1 lựa chọn trong nhóm → dùng cho chọn phương thức thanh toán.
4.type="checkbox" → hộp kiểm để tích chọn, có thể sử dụng required để bắt buộc → dùng cho việc đồng ý với các điều khoản sử dụng.
5.type="search" → ô nhập text có nút xóa nhanh (x) để tối ưu trải nghiệm tìm kiếm → dùng cho thanh tìm kiếm sản phẩm.
6.type="date" → mở hộp thoại lịch để người dùng chọn ngày/tháng/năm → dùng để chọn ngày giao hàng hoặc ngày hẹn.
7.type="tel" → ô nhập văn bản đơn giản nhưng tối ưu hóa bàn phím số trên di động → dùng để nhập số điện thoại người nhận hàng.
8.type="number" → ô nhập liệu số có nút tăng/giảm, kiểm soát được giới hạn min/max → dùng để chọn số lượng sản phẩm trong giỏ hàng.
9.type="password" → ô nhập văn bản bị che ẩn ký tự để bảo mật thông tin → dùng để nhập mật khẩu đăng nhập.
10.type="email" → ô nhập text có kiểm tra cấu trúc email, tự động kích hoạt bàn phím @ trên di động → dùng cho form đăng ký tài khoản.
Câu A2
Th1:Browser chặn submit và hiện tb "Vui lòng điền vào th này" vì có required bị để trống
Th2:Browser chặn submit vì "abc" ko có @, hiện tb"Vui lòng nhập địa chỉ gmail"
Th3:Browser chặn submit vì 15 lớn hơn 10, tb"Giá trị phải nhỏ hơn hoặc bằng 10"
Th4:Browser chặn submit vì "abc123" không khớp với pattern đúng 10 chữ số
Th5:Browser chặn submit vì "123" chỉ có 3 ký tự ,ko đủ minlength = "8"