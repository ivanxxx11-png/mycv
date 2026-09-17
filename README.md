# Hồ sơ cá nhân — Vũ Nguyễn Gia Bảo

Website tĩnh giới thiệu bản thân (hồ sơ cá nhân), xây dựng bằng HTML5 và CSS3 thuần (không dùng framework), theo yêu cầu bài tập "Xây dựng website tĩnh".

## Cấu trúc thư mục

```
project/
├── index.html          # Trang chủ
├── about.html          # Giới thiệu bản thân, kỹ năng, học vấn
├── projects.html       # Danh sách dự án cá nhân
├── contact.html        # Thông tin liên hệ + form
├── css/
│   └── style.css       # Toàn bộ CSS dùng chung cho 4 trang
├── images/
│   ├── favicon.svg
│   ├── avatar.svg
│   ├── project-trangsach.svg
│   ├── project-nhipngay.svg
│   └── project-sanchoi.svg
└── README.md
```

Tất cả liên kết nội bộ, ảnh và CSS đều dùng **đường dẫn tương đối** (ví dụ `css/style.css`, `images/avatar.svg`, `about.html`) để website chạy đúng cả khi mở trực tiếp trên máy lẫn khi triển khai trên GitHub Pages.

## Nguồn tài nguyên bên ngoài

- Font chữ **Fraunces** và **Work Sans**: tải qua Google Fonts (https://fonts.google.com), được nhúng bằng thẻ `<link>` trong phần `<head>` mỗi trang.
- Toàn bộ hình minh họa (`images/*.svg`) do tác giả tự vẽ bằng SVG, không sử dụng ảnh/tư liệu của bên thứ ba.

## Cách chạy thử trên máy cá nhân

Không cần cài đặt gì thêm — chỉ cần mở file `index.html` bằng trình duyệt. Để có trải nghiệm giống môi trường server thật (khuyến khích khi kiểm tra đường dẫn tương đối), có thể dùng một server tĩnh đơn giản, ví dụ:

```bash
# Python 3
python3 -m http.server 8000
# rồi mở http://localhost:8000
```

## Hướng dẫn đưa mã nguồn lên GitHub và bật GitHub Pages

1. Tạo một repository mới trên GitHub (ví dụ đặt tên `ho-so-ca-nhan`).
2. Trong thư mục `project/` (thư mục gốc chứa `index.html`), chạy:
   ```bash
   git init
   git add .
   git commit -m "Khởi tạo website hồ sơ cá nhân"
   git branch -M main
   git remote add origin https://github.com/<ten-tai-khoan>/<ten-repo>.git
   git push -u origin main
   ```
3. Vào repository trên GitHub → **Settings** → mục **Pages** (bên trái).
4. Ở phần **Build and deployment**, chọn **Source: Deploy from a branch**, chọn **Branch: main**, thư mục **/ (root)**, rồi bấm **Save**.
5. Chờ khoảng 1–2 phút, GitHub sẽ hiển thị đường dẫn dạng:
   ```
   https://<ten-tai-khoan>.github.io/<ten-repo>/
   ```
6. Mở đường dẫn đó, kiểm tra lần lượt cả 4 trang và trên cả điện thoại lẫn máy tính để chắc chắn không có liên kết hay hình ảnh bị lỗi.
7. Ghi đường dẫn này vào file `duong-dan-website.txt` để nộp bài.

## Kiểm tra trước khi nộp

- [ ] Cả 4 trang đều có tiêu đề, thanh điều hướng, nội dung chính và chân trang thống nhất.
- [ ] Các liên kết giữa 4 trang hoạt động đúng (không có link 404).
- [ ] Ảnh hiển thị đầy đủ, có thuộc tính `alt` mô tả.
- [ ] Giao diện hiển thị tốt trên màn hình máy tính và điện thoại (đã kiểm tra bằng cách thu nhỏ trình duyệt / chế độ responsive của DevTools).
- [ ] Website đã publish thành công qua GitHub Pages và có thể truy cập công khai.
