# Hướng dẫn đưa website lên GitHub Pages

## Bước 1 — Chuẩn bị
1. Tạo tài khoản/đăng nhập GitHub.
2. Cá nhân hóa `index.html` và kiểm thử theo `TEST_CHECKLIST.md`.
3. Đổi tên thư mục nếu muốn cho dễ quản lý; tên repository trên GitHub phải theo mẫu đề bài: `Ten_Ho_MSSV` (thay bằng tên/họ/MSSV thật).

## Bước 2 — Tạo repository
1. Vào https://github.com/new
2. Repository name: `Ten_Ho_MSSV` theo đúng quy định trong PDF.
3. Chọn **Public** để giảng viên truy cập thuận tiện.
4. Có thể tạo README trên GitHub hoặc không; nếu đã có source local thì nên tránh tạo thêm file trùng tên gây xung đột.
5. Chọn **Create repository**.

## Bước 3 — Đưa source lên GitHub bằng giao diện web (cách dễ cho người mới)
1. Mở repository vừa tạo.
2. Chọn **Add file → Upload files**.
3. Kéo các file/thư mục bên trong project lên, gồm `index.html`, `css/`, `js/`, `PROMPT_LOG.md`, `README.md`, `TEST_CHECKLIST.md`, `GITHUB_PAGES_GUIDE.md`.
4. Lưu ý: `index.html` phải ở ngay thư mục gốc repository, không nằm sâu trong một thư mục con.
5. Nhập commit message, ví dụ `Add portfolio website source`, rồi chọn **Commit changes**.
6. Nếu giao diện GitHub không cho upload nguyên thư mục, tạo thư mục/file bằng cách upload file bên trong hoặc dùng GitHub Desktop/VS Code.

## Bước 4 — Bật GitHub Pages
1. Vào **Settings** của repository.
2. Mở mục **Pages** ở thanh bên.
3. Trong **Build and deployment**, chọn **Deploy from a branch**.
4. Chọn branch `main` (hoặc branch đang chứa source) và folder `/(root)`.
5. Chọn **Save**.
6. Chờ GitHub build và xuất hiện đường dẫn trang. Thường URL có dạng `https://TEN-TAI-KHOAN.github.io/TEN-REPOSITORY/`; hãy dùng URL chính xác GitHub hiển thị, không tự đoán tên tài khoản.

## Bước 5 — Kiểm tra và nộp
1. Mở link GitHub Pages được cung cấp trong Settings → Pages.
2. Thử mở trang bằng cửa sổ ẩn danh hoặc điện thoại.
3. Kiểm tra menu, các mục điều hướng, layout mobile và hiệu ứng (CDN cần Internet).
4. Đưa URL GitHub repository và URL GitHub Pages vào nơi nộp bài theo yêu cầu của giảng viên.
5. Có thể thêm URL demo vào phần **About** hoặc mô tả repository.

## Nếu trang bị lỗi
- **404:** kiểm tra `index.html` ở root, branch/folder Pages đã chọn đúng và đợi build hoàn tất.
- **CSS không tải:** kiểm tra đường dẫn tương đối `css/style.css` và chữ hoa/thường của tên file.
- **JavaScript không tải:** kiểm tra `js/main.js` và Console của trình duyệt.
- **AOS/Animate.css không chạy:** kiểm tra kết nối Internet, CDN và lỗi Console/Network.
- **Trang hiển thị source thay vì giao diện:** xác nhận mở đúng URL Pages và file `index.html` là HTML hợp lệ.
