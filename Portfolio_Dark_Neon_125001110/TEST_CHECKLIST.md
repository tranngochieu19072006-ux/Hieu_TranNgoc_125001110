# Checklist kiểm thử trước khi nộp

> Chỉ đánh dấu `[x]` sau khi tự thực hiện và xác nhận. Không dùng checklist này để khẳng định đã kiểm thử nếu chưa chạy trang.

## A. HTML5 semantic — theo đề thi
- [ ] Có `<header>` chứa logo và điều hướng.
- [ ] Có `<nav>` cho điều hướng.
- [ ] Có `<main>` chứa nội dung chính.
- [ ] Có nhiều `<section>` và có `<article>` cho nội dung độc lập.
- [ ] Có `<footer>`.
- [ ] Các phần tử được dùng đúng mục đích, không thay toàn bộ bằng `div`.

## B. CSS / UI / UX
- [ ] Có `:root` và các CSS variables như `--primary-color`.
- [ ] Bố cục dùng Flexbox và CSS Grid.
- [ ] Mở trên desktop (ví dụ 1366×768) không bị tràn ngang.
- [ ] Mở ở tablet (ví dụ 768×1024) bố cục vẫn rõ.
- [ ] Mở trên điện thoại (ví dụ 390×844) không bị tràn ngang; menu mobile hoạt động.
- [ ] Nút, thẻ dự án và liên kết có trạng thái hover.
- [ ] Dùng Tab để di chuyển và xác nhận focus nhìn thấy rõ.
- [ ] Chữ dễ đọc, độ tương phản ổn, khoảng cách không bị chật.

## C. Animate.css / AOS
- [ ] Hiệu ứng Animate.css xuất hiện ở phần hero.
- [ ] Cuộn xuống: các phần có `data-aos` xuất hiện đúng.
- [ ] Không có lỗi tải CDN trong Console/Network (nếu có Internet).
- [ ] Hiệu ứng không quá nhiều hoặc gây khó đọc.
- [ ] Tôn trọng thiết lập giảm chuyển động của hệ điều hành.

## D. JavaScript / liên kết
- [ ] Menu mobile mở và đóng khi bấm nút.
- [ ] Chọn mục menu trên mobile thì menu tự đóng.
- [ ] Năm ở footer tự cập nhật.
- [ ] Email, GitHub và LinkedIn đã thay bằng thông tin thật.
- [ ] Các liên kết không còn URL placeholder không mong muốn.

## E. GitHub / nộp bài
- [ ] Tên repository đúng định dạng `Ten_Ho_MSSV`.
- [ ] Đã đẩy `index.html`, `css/`, `js/`, `PROMPT_LOG.md`, `README.md` và checklist.
- [ ] Có commit message dễ hiểu.
- [ ] Đã bật GitHub Pages từ branch/folder đúng.
- [ ] Link GitHub Pages mở được ở cửa sổ ẩn danh hoặc thiết bị khác.
- [ ] Đã cập nhật nhật ký prompt và ghi trung thực kết quả kiểm thử.

## Ghi chú lỗi phát hiện và cách sửa
| Ngày | Lỗi/vấn đề | Cách xử lý | Đã kiểm tra lại? |
|---|---|---|---|
| [ngày] | [ghi lỗi thật nếu có] | [ghi cách sửa thật] | [Có/Không] |
