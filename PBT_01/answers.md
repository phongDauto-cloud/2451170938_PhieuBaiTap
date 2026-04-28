Câu A1:  
a)Các bước xảy ra gồm:

1. Request đi từ laptop đến router tại nhà
2. Sau đó đi qua IPS
3.chạy đến server của shoppe thông qua cáp quang
4.Server xử lý request hiển thị lên Homepage
5.Sau đó repsonse được Server gửi ngược lại laptop
6.Trình duyệt nhận tập file HTML, CSS, JS sau đó render ra giao diện Homepage
b) Tab network trong devtool của Chrome cho ta thấy:
![alt text](<PBT_01/screenshots/Screenshot 2026-04-22 185658.png>)

- Danh sách các request
- Chi tiết các thông tin của 1 request
- Các tài nguyên được gửi về (CSS,JS, IMG, FONT, etc)

Câu A2:
 Các lỗi semantic là: Trang web bị GG đánh lỗi SEO thấp do, mắc phải các lỗi semantic, dùng các thẻ chưa đúng và chưa hợp lý, khiến cho trang web không được đánh giá cao.

Các lỗi semantic trong trang web là

Title của sản phẩm lại dùng thẻ div <div>, thay vào đó nên dùng thẻ heading để làm nổi bật tên sản phẩm

<div class="title">iPhone 16 Pro</div>
sửa

<h2 class="title">iPhone 16 Pro</h2>
Khung bao bọc phần quan trọng nhất của trang web (sản phẩm) lại được bọc trong thẻ div với class là main<div class="main">, nên dùng thẻ main để trình duyệt biết dược đây là phần quan trọng nhất của trang web để tối ưu semantic

<div class=main>...</div>
sửa

<main>...</main>
Thay vì bao bọc sản phẩm(product) bằng một thẻ div<div class="product">, ta thấy mỗi sản phẩm có thể là một nội dung riêng biệt, nên có thể dùng thẻ article để tối ưu.

<div class="product">...</div>
sửa

<article class="title">...</article>
Ở phần giá tiền, ta thấy trang web đang dùng thẻ <div class="price">, nhưng thực tế giá tiền đó là một giá trị vậy để tối ưu ta có thể dùng thẻ data để hiển thị.

<div class="price">25.990.000đ</div>
sửa

<data value="2599000">25.990.000đ</data>

Câu A3 Kết quả hiển thị

--------------------------------
|Hộp 1                         |
|Text A Text B                 |
|Hộp 2                         |
|Text C Text D                 |
|Hộp 3                         |
|                              |
|                              |
|                              |
--------------------------------
Giải thích

đối với các thẻ như <div> thì render ra trên browser text trong các thẻ sẽ xuống dòng vì vậy các nội dung như Hộp 1, Hộp 2 và Hộp 3 mới ở mỗi cái một dòng, tương tự với nội dung được bao bọng trong các thẻ đó

đối với các thẻ như <span> thì thẻ này hoàn toàn có thể render trên cùng 1 dòng với các thẻ nội dung khác như vì vậy các nội dung như "Text A", "Text B" mới có thể đứng cùng 1 dòng đối với thẻ <strong> thẻ này render tương tự như thẻ <span> có thể ở cùng dòng với các nội dung khác nhưng thẻ này có nhiệm vụ in đậm text bên trong và nói cho browser biết đây là nội dung cần được chú ý.

Câu A4 - Table


05_tables_hyperlinks.md — Mục Table — Bảng dữ liệu
04_visible_part_html.md — Mục Bản đồ Semantic Elements
1. Sự khác nhau giữa <thead>, <tbody>, <tfoot>
<thead>: Phần đầu bảng, thường chứa tiêu đề cột.
<tbody>: Phần thân bảng, chứa dữ liệu chính.
<tfoot>: Phần chân bảng, thường chứa tổng kết hoặc ghi chú.
Việc chia rõ ba phần giúp trình duyệt, máy in, screen reader và lập trình viên hiểu cấu trúc bảng tốt hơn.

2. Tại sao KHÔNG nên dùng table để tạo layout trang web?
Khó responsive: Bảng có cấu trúc cứng, khó thích nghi trên điện thoại.
Accessibility kém: Screen reader hiểu table là dữ liệu dạng bảng, không phải bố cục trang.
Code rối và khó bảo trì: Dùng nhiều <table>, <tr>, <td> lồng nhau khiến mã dài và khó sửa.
Không đúng mục đích: Table sinh ra để hiển thị dữ liệu dạng hàng/cột, không phải để dàn trang.

Bài B3 — Debug HTML (Phân tích và sửa 12 lỗi)

Dưới đây là danh sách 12 lỗi đã được phát hiện và khắc phục trong file debug.html:

Lỗi 1: Dòng 1 — Khai báo <!DOCTYPE> không đầy đủ — Sửa: <!DOCTYPE html>.
Lỗi 2: Dòng 2 — Thẻ <html> thiếu thuộc tính lang (quan trọng cho Accessibility) — Sửa: <html lang="vi">.
Lỗi 3: Dòng 4 — Thẻ <title> chưa có thẻ đóng — Sửa: Thêm </title>.
Lỗi 4: Dòng 5 — Thiếu thẻ <meta name="viewport"> khiến trang không hiển thị tốt trên di động — Sửa: Bổ sung meta viewport.
Lỗi 5: Dòng 5 — Giá trị charset utf8 viết sai định dạng chuẩn — Sửa: UTF-8.
Lỗi 6: Dòng 8 — Thẻ <h1> sử dụng thẻ đóng sai — Sửa: </h1>.
Lỗi 7: Dòng 12 — Thẻ <a> đầu tiên đóng sai cú pháp — Sửa: </a>.
Lỗi 8: Dòng 21 — Thẻ <img> thiếu ngoặc kép cho thuộc tính và thiếu alt mô tả ảnh — Sửa: Thêm ngoặc kép và alt.
Lỗi 9: Dòng 23 — Lồng thẻ sai quy tắc (thẻ <b> đóng sau thẻ <p>) — Sửa: Đóng <b> trước khi đóng <p>.
Lỗi 10: Dòng 30-31 — Hàng tiêu đề bảng sử dụng thẻ <td> thay vì <th> — Sửa: Thay bằng <th> để đúng ngữ nghĩa tiêu đề.
Lỗi 11: Dòng 28-37 — <table> thiếu cấu trúc <thead> và <tbody> — Sửa: Bổ sung các thẻ phân đoạn bảng.
Lỗi 12: Dòng 41 — Sử dụng hai thẻ <main> trên cùng một trang (sai chuẩn HTML5) — Sửa: Thay thẻ <main> thứ hai thành <aside>.
Lỗi 13: Dòng 46 — Thẻ <p> trong footer chưa được đóng — Sửa: Thêm </p>.

Bài B2 — Debug HTML (Tìm và sửa 11 lỗi)

Danh sách lỗi tìm được trong file HTML:

Lỗi 1: Dòng 1 — Khai báo <!DOCTYPE> không đầy đủ — Cách sửa: <!DOCTYPE html>

Lỗi 2: Dòng 3 — Thẻ <title> chưa có thẻ đóng </title> — Cách sửa: <title>Trang web</title>

Lỗi 3: Dòng 4 — Giá trị charset sai chuẩn (utf8) — Cách sửa: <meta charset="UTF-8">

Lỗi 4: Dòng 8 — Thẻ <h1> đóng sai (dùng <h1> thay vì </h1>) — Cách sửa: <h1>Welcome to ShopTLU</h1>

Lỗi 5: Dòng 11 — Thẻ <a> đóng sai (dùng <a> thay vì </a>) — Cách sửa: <a href="home">Trang chủ</a>

Lỗi 6: Dòng 16 — Thuộc tính src không có ngoặc kép — Cách sửa: <img src="iphone.jpg" alt="iPhone 16 Pro">

Lỗi 7: Dòng 16 — Thẻ <img> thiếu thuộc tính alt (semantic) — Cách sửa: Thêm alt="iPhone 16 Pro"

Lỗi 8: Dòng 18 — Lồng thẻ sai (</b> đóng sau </p>) — Cách sửa: <p>Giá: <b>25.990.000đ</b></p>

Lỗi 9: Dòng 23-32 — Bảng <table> thiếu cấu trúc <thead> và <tbody> — Cách sửa: Bọc hàng tiêu đề trong <thead> và dữ liệu trong <tbody>

Lỗi 10: Dòng 23 — Hàng tiêu đề bảng dùng <td> thay vì <th> — Cách sửa: <th>Tên</th> và <th>Giá</th>

Lỗi 11: Dòng 34 — Có 2 thẻ <main> trên cùng trang (sai chuẩn HTML5) — Cách sửa: Thay thẻ <main> thứ 2 thành <aside>

Lỗi 12: Dòng 37 — Thẻ <p> trong footer chưa đóng </p> — Cách sửa: <p>Copyright 2026</p>

Câu C1 - Thiết kế cấu trúc HTML

<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>C1 — Chi tiết sản phẩm</title>
</head>
<body>

<header>
    <!-- header: phần đầu trang -->
    <nav>
        <!-- nav: khu vực điều hướng chính -->
        <ul>
            <li><a href="/">Trang chủ</a></li>
            <li><a href="/cart">Giỏ hàng</a></li>
        </ul>
    </nav>
</header>

<nav aria-label="breadcrumb">
    <!-- nav: breadcrumb là một dạng điều hướng -->
    <ol>
        <!-- ol: breadcrumb có thứ tự cấp bậc -->
        <li><a href="/">Trang chủ</a></li>
        <li><a href="/dien-thoai">Điện thoại</a></li>
        <li>iPhone 16</li>
    </ol>
</nav>

<main>
    <!-- main: nội dung chính của trang -->

    <article>
        <!-- article: khối nội dung độc lập về sản phẩm -->

        <section id="gallery">
            <!-- section: nhóm khu vực ảnh sản phẩm lại thành 1 phân đoạn riêng -->
            <h2>Hình ảnh sản phẩm</h2>

            <figure>
                <!-- figure: ảnh chính của sản phẩm kèm chú thích -->
                <img src="https://placehold.co/600x400" alt="iPhone 16 Pro Max - Ảnh chính">
                <figcaption>iPhone 16 Pro Max — Ảnh chính</figcaption>
            </figure>

            <figure>
                <img src="https://placehold.co/600x400" alt="iPhone 16 Pro Max - Góc nghiêng">
                <figcaption>Góc nghiêng</figcaption>
            </figure>

            <figure>
                <img src="https://placehold.co/600x400" alt="iPhone 16 Pro Max - Mặt sau">
                <figcaption>Mặt sau</figcaption>
            </figure>

            <figure>
                <img src="https://placehold.co/600x400" alt="iPhone 16 Pro Max - Camera">
                <figcaption>Cụm camera</figcaption>
            </figure>

            <figure>
                <img src="https://placehold.co/600x400" alt="iPhone 16 Pro Max - Hộp sản phẩm">
                <figcaption>Hộp sản phẩm</figcaption>
            </figure>
        </section>

        <section id="info">
            <!-- section: nhóm thông tin sản phẩm riêng -->
            <h1>iPhone 16 Pro Max</h1>
            <p><strong>25.990.000đ</strong></p>
            <p>⭐⭐⭐⭐⭐</p>
            <p>Mô tả sản phẩm...</p>
        </section>

        <section id="specs">
            <!-- section: khu vực thông số kỹ thuật -->
            <h2>Thông số kỹ thuật</h2>
            <table>
                <thead>
                    <tr>
                        <th>Thông số</th>
                        <th>Chi tiết</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>Chip</td>
                        <td>A18 Pro</td>
                    </tr>
                </tbody>
            </table>
        </section>

        <section id="reviews">
            <!-- section: khu vực đánh giá -->
            <h2>Đánh giá</h2>
            <p><em>(Chưa có đánh giá)</em></p>
        </section>

    </article>

    <aside>
        <!-- aside: nội dung phụ — sản phẩm tương tự -->
        <h2>Sản phẩm tương tự</h2>
        <p><em>(Placeholder)</em></p>
    </aside>

</main>

<footer>
    <!-- footer: phần cuối trang -->
    <p>&copy; 2026 ShopTLU</p>
</footer>

</body>
</html>

Câu C2 - So sánh & Tranh luận

Quan điểm “dùng <div> cho mọi thứ rồi thêm class là đủ” có thể giúp viết code nhanh lúc đầu, nhưng về lâu dài sẽ tạo ra nhiều vấn đề kỹ thuật. Semantic HTML không phải học thêm cho có, mà là nền tảng quan trọng của web hiện đại.

Thứ nhất, về SEO. Công cụ tìm kiếm như Google không nhìn giao diện CSS mà đọc cấu trúc HTML. Khi dùng các thẻ như <header>, <nav>, <main>, <article>, Google dễ hiểu đâu là nội dung chính, đâu là menu, đâu là phần phụ. Điều đó giúp trang web được index tốt hơn và cải thiện thứ hạng tìm kiếm.

Thứ hai, về Accessibility. Người khiếm thị sử dụng screen reader để truy cập web. Các phần mềm này dựa vào semantic tags để cho phép người dùng nhảy nhanh đến menu (<nav>), nội dung chính (<main>), hay bài viết (<article>). Nếu toàn bộ trang chỉ là <div>, trải nghiệm sử dụng sẽ rất kém.

Ví dụ thực tế: Chế độ Reader View trên Safari hoặc Edge thường dựa vào cấu trúc semantic để tách nội dung bài viết khỏi quảng cáo và menu. Nếu website dùng đúng <article>, tính năng này hoạt động hiệu quả hơn.

Tuy nhiên, <div> vẫn rất cần thiết trong nhiều trường hợp. Ví dụ, khi cần tạo một khối wrapper để dùng Flexbox hoặc Grid phục vụ bố cục giao diện mà khối đó không mang ý nghĩa nội dung, dùng <div> là hoàn toàn hợp lý.