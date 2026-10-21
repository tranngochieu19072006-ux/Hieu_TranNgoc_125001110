# NHẬT KÝ PROMPT ENGINEERING (VIBE CODING LOG)

## Thông tin sinh viên
- **Họ và tên:** [Điền họ và tên của bạn]
- **MSSV:** 125001110
- **Chủ đề website:** Portfolio cá nhân — Dark hiện đại, đen và tím neon
- **Công cụ AI sử dụng:** ChatGPT (hỗ trợ lên cấu trúc, viết mã và rà soát); [bổ sung công cụ khác nếu thực sự sử dụng]

> **Ghi chú trung thực:** Nhật ký dưới đây ghi lại các prompt được dùng/đề xuất trong quá trình tạo project này và các bước kiểm tra dự kiến. Hãy chỉnh sửa phần “kết quả thực tế” sau khi tự chạy và kiểm thử trên máy của bạn; không ghi rằng đã kiểm tra hoặc sửa lỗi nếu bạn chưa thực hiện bước đó.

## 1. Prompt ban đầu (Initial Prompt)

**Prompt đã dùng:**

> Bắt đầu thực hiện đề thi giữa kỳ Thiết kế Web theo PDF đã gửi. Chủ đề: Portfolio cá nhân. Phong cách: Dark hiện đại, đen và tím neon. MSSV: 125001110. Bám sát toàn bộ tiêu chí trong đề gốc, tạo source chạy được, PROMPT_LOG.md trung thực với quá trình làm, README, checklist kiểm thử và hướng dẫn GitHub Pages. Bắt đầu bằng việc dựng và đóng gói project hoàn chỉnh.

**Mục tiêu của prompt:**
- Dựng website portfolio cá nhân theo phong cách dark/neon tím.
- Đáp ứng yêu cầu HTML5 semantic, CSS variables, Flexbox/Grid, responsive, Animate.css, AOS, hover/focus.
- Có nhật ký prompt, README, checklist và hướng dẫn xuất bản GitHub Pages.

**Kết quả tạo ra trong project:**
- `index.html`: trang portfolio với header/nav/main/section/article/footer.
- `css/style.css`: thiết kế responsive, CSS custom properties, Grid/Flexbox và trạng thái hover/focus.
- `js/main.js`: menu mobile và năm hiện tại.
- `PROMPT_LOG.md`, `README.md`, `TEST_CHECKLIST.md`, `GITHUB_PAGES_GUIDE.md`.

## 2. Quá trình lặp và cải tiến (Iterations)

### Lần 1 — Semantic HTML5 & CSS Variables

**Prompt/tiêu chí sử dụng:**

> Rà soát cấu trúc trang theo HTML5 semantic. Đảm bảo có header chứa logo và điều hướng, nav, main, section/article và footer. Dùng :root để khai báo màu sắc, font, khoảng cách, bo góc; dùng Flexbox/Grid cho layout responsive. Tránh dùng div thay cho các phần tử có ngữ nghĩa phù hợp.

**Kết quả trong mã nguồn:**
- Dùng `<header>`, `<nav>`, `<main>`, `<section>`, `<article>` và `<footer>`.
- Khai báo các biến như `--primary-color`, `--bg-color`, `--text-color`, `--font-family`, `--space-*`, `--radius-*` trong `:root`.
- Dùng CSS Grid cho hero, kỹ năng và dự án; Flexbox cho header, nav, nút và footer.

**Tự đánh giá / chỉnh sửa của sinh viên (hãy cập nhật sau khi kiểm tra):**
- [ ] Mình đã mở `index.html` và xác nhận đủ các thẻ semantic.
- [ ] Mình đã đổi “Your Name” và nội dung mẫu thành thông tin thật.
- [ ] Ghi chú điểm cần cải tiến sau khi tự xem mã: [điền tại đây].

### Lần 2 — Animate.css & AOS

**Prompt/tiêu chí sử dụng:**

> Tích hợp Animate.css cho các thành phần hero chính và AOS cho các section/card khi cuộn trang. Hiệu ứng nên nhẹ, có kiểm soát, không gây rối mắt; cấu hình AOS một lần khi DOM sẵn sàng. Đảm bảo website vẫn đọc được nếu JavaScript hoặc thư viện ngoài không tải.

**Kết quả trong mã nguồn:**
- Animate.css được tải từ CDN và áp dụng cho eyebrow, tiêu đề, mô tả và CTA ở hero.
- AOS được tải từ CDN; các section/card có `data-aos`; khởi tạo bằng `AOS.init(...)` khi DOM sẵn sàng.
- Có `prefers-reduced-motion` để giảm chuyển động theo cài đặt của hệ điều hành.

**Vấn đề cần xác minh khi chạy thật:**
- CDN cần kết nối Internet; nếu Animate.css/AOS không tải, các hiệu ứng thư viện có thể không hoạt động.
- Nếu AOS không hoạt động khi cuộn, kiểm tra tab Network/Console, đường dẫn CDN, lỗi JavaScript và bảo đảm `AOS.init()` chạy sau khi thư viện được tải.

**Prompt gỡ lỗi mẫu — chỉ ghi là đã dùng nếu bạn thực sự chạy và gặp lỗi:**

> AOS không kích hoạt khi cuộn trang. Hãy giúp mình kiểm tra thứ tự tải thư viện, thuộc tính `data-aos`, lỗi Console và vị trí gọi `AOS.init()`. Đề xuất thay đổi nhỏ nhất và giải thích nguyên nhân.

**Kết quả gỡ lỗi thực tế:** [Chưa ghi nhận — điền sau khi tự kiểm tra, nếu có.]

### Lần 3 — Responsive, hover/focus và JavaScript

**Prompt/tiêu chí sử dụng:**

> Rà soát giao diện ở màn hình desktop và điện thoại. Menu mobile phải mở/đóng được, tự đóng sau khi chọn liên kết; nút/card có hover; liên kết và nút có focus-visible rõ ràng. Không thêm tương tác giả cho các liên kết chưa có đích thật.

**Kết quả trong mã nguồn:**
- CSS có breakpoint tại 950px, 700px và 390px.
- Menu mobile có `aria-expanded`, có thể mở/đóng và tự đóng khi chọn mục.
- Có `:hover`, `:focus-visible` và hỗ trợ `prefers-reduced-motion`.
- Các dự án là nội dung mẫu; cần thay bằng dự án thật và URL tương ứng trước khi nộp.

**Kết quả kiểm tra thực tế:** [Điền các trình duyệt/kích thước màn hình đã thử và lỗi đã sửa. Không đánh dấu đạt nếu chưa thử.]

## 3. Tự đánh giá (Personal Assessment)

**AI giúp tiết kiệm thời gian như thế nào?**
- AI hỗ trợ dựng nhanh bộ khung HTML, đề xuất hệ thống biến CSS và tạo các breakpoint ban đầu.
- AI giúp phác thảo hiệu ứng chuyển động và JavaScript cho menu mobile, để sinh viên dành thêm thời gian đọc mã, kiểm thử và tùy chỉnh.

**Bài học rút ra về Prompt Engineering cho thiết kế web:**
- Prompt càng nêu rõ tiêu chí nghiệm thu (thẻ semantic bắt buộc, tên biến, thư viện hiệu ứng, breakpoint, trạng thái hover/focus), kết quả càng dễ đối chiếu với đề.
- Nên chia yêu cầu lớn thành các vòng: cấu trúc HTML → phong cách CSS → hiệu ứng → responsive → kiểm thử.
- Không nên tin ngay kết quả AI: phải chạy trang, kiểm tra Console/Network, thử liên kết và xem giao diện ở nhiều kích thước.
- Nhật ký prompt cần phản ánh đúng việc đã làm. Phân biệt rõ mã được sinh, bước đã kiểm tra và lỗi thực tế đã gặp.

## 4. Việc sinh viên cần hoàn tất trước khi nộp
1. Thay `[Điền họ và tên của bạn]`, `Your Name`, email và liên kết mạng xã hội bằng thông tin thật.
2. Thay 3 dự án minh họa bằng dự án của bản thân hoặc ghi rõ đó là bài thực hành.
3. Thực hiện toàn bộ checklist trong `TEST_CHECKLIST.md` và cập nhật kết quả thật.
4. Tạo repository đúng định dạng `Ten_Ho_MSSV`, đẩy source và bật GitHub Pages.
5. Kiểm tra link công khai trong cửa sổ ẩn danh/thiết bị khác trước khi nộp.
