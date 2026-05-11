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

Câu A3
<label for="email"> quan trọng vì screen reader đọc đúng nhãn của ô nhập, và người dùng click vào label cũng focus vào input tương ứng.
<fieldset> + <legend> dùng để nhóm các trường liên quan, ví dụ nhóm “Thông tin cá nhân” trong form đăng ký.
aria-label dùng khi phần tử không có text mô tả nhìn thấy được, ví dụ nút icon chỉ có biểu tượng. Không nên dùng aria-label khi đã có <label> vì dễ gây trùng nghĩa hoặc che mất nhãn thật, làm giảm accessibility và bảo trì khó hơn.

Câu A4
loading="lazy" trên <img> giúp trì hoãn tải ảnh cho đến khi ảnh gần vào vùng nhìn thấy, giảm tải ban đầu và cải thiện tốc độ. Không nên dùng cho ảnh quan trọng ở ngay đầu trang hoặc ảnh hero cần hiển thị ngay.
Nên cung cấp nhiều <source> trong <video> để tăng khả năng tương thích trình duyệt. Ba format phổ biến: mp4, webm, ogg.
alt dùng để mô tả nội dung ảnh cho người dùng khi ảnh lỗi, cho screen reader và cho SEO.
Ví dụ alt tốt:

Ảnh sản phẩm iPhone 16 → alt="iPhone 16 màu đen, chụp góc nghiêng mặt trước"
Ảnh trang trí → alt="" để bỏ qua với ảnh decorative
Ảnh biểu đồ doanh thu Q1/2026 → alt="Biểu đồ doanh thu quý 1 năm 2026 tăng từ 120 đến 180 tỷ đồng"

Câu A5:
Khi nào dùng Cách 1?
Dùng <img> đơn lẻ khi ảnh chỉ là một phần minh hoạ ngắn, không cần chú thích riêng.
Ví dụ:
    Ảnh avatar người dùng
    Ảnh icon thanh toán
Khi nào dùng Cách 2?
Dùng <figure> + <figcaption> khi ảnh và chú thích đi cùng nhau như một đơn vị nội dung.

Ví dụ:
    Ảnh sản phẩm kèm giá
    Ảnh biểu đồ kèm ghi chú dữ liệu

Câu C1
Lỗi 1: Input “Tên” không có <label for="...">, vi phạm accessibility.

Sửa:

<label for="name">Tên:</label>
<input type="text" id="name" name="name" required placeholder="Nhập tên của bạn">
Lỗi 2: Input email thiếu label, thiếu name, thiếu required.

Sửa:

<label for="email">Email:</label>
<input type="email" id="email" name="email" required placeholder="Email của bạn">
Lỗi 3: Mật khẩu chưa có label, name, minlength và required.

Sửa:

<label for="password">Mật khẩu:</label>
<input type="password" id="password" name="password" required minlength="8" placeholder="Mật khẩu">
Lỗi 4: Ô nhập lại mật khẩu chưa có label và HTML không thể tự kiểm tra khớp với mật khẩu trước.

Sửa:

<label for="confirm-password">Nhập lại mật khẩu:</label>
<input type="password" id="confirm-password" name="confirm-password" required minlength="8" placeholder="Nhập lại mật khẩu">
Lỗi 5: Phone dùng type="text" với value cố định, thiếu label, thiếu pattern, thiếu name.

Sửa:

<label for="phone">Phone:</label>
<input type="tel" id="phone" name="phone" pattern="[0-9]{10}" placeholder="0901234567" required>
Lỗi 6: <select> chưa có label và không có name.

Sửa:

<label for="city">Thành phố:</label>
<select id="city" name="city" required>
  <option value="">-- Chọn thành phố --</option>
  <option value="hn">Hà Nội</option>
  <option value="hcm">TP.HCM</option>
</select>
Lỗi 7: Điều khoản chỉ có <label> rỗng, chưa có checkbox để người dùng tick.

Sửa:

<label for="agree">
  <input type="checkbox" id="agree" name="agree" required>
  Tôi đồng ý điều khoản
</label>
Lỗi 8: Nút submit ổn, nhưng form nên có action, method và các trường nên có name để gửi dữ liệu đúng.

Sửa:

<form action="#" method="POST"> 
Câu C2
Pattern regex:
CMND/CCCD 12 chữ số: pattern="[0-9]{12}"
Số tài khoản 10–15 chữ số: pattern="[0-9]{10,15}"
HTML5 validation không đủ an toàn cho ngân hàng số vì chỉ chạy ở frontend, người dùng có thể tắt JS, sửa HTML, hoặc gửi request trực tiếp. Phải validate lại ở backend.

3 loại validation HTML5 không thể làm tốt:

So sánh 2 ô nhập với nhau, ví dụ xác nhận mật khẩu
Kiểm tra dữ liệu có tồn tại trong database, ví dụ số tài khoản đã đăng ký chưa
Kiểm tra logic nghiệp vụ hoặc API, ví dụ OTP đúng hạn, số dư đủ, PIN đã bị khóa chưa
2 rủi ro nếu chỉ validate frontend:
Dữ liệu sai hoặc độc hại có thể đi thẳng vào hệ thống
Kẻ xấu có thể bypass validation và khai thác API/backend bằng request giả