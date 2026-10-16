# WebGọn

Trang báo giá website, SEO và tích hợp AI bằng tiếng Việt. HTML, CSS và JavaScript thuần; không cần cài thư viện hoặc build.

## Chạy trên máy

Chạy `python -m http.server 4173 --directory dist`, sau đó mở http://localhost:4173.

## Kiểm tra

```sh
node --check dist/app.js
node verify-pricing.cjs
```

## Triển khai GitHub Pages

Trong repository, chọn **Settings → Pages → Build and deployment → Source → GitHub Actions**. Workflow `Deploy WebGon to GitHub Pages` chạy khi đẩy lên nhánh `main`; có thể chạy lại từ tab Actions.

Đường dẫn dự kiến sau khi workflow thành công: https://kingboylegend.github.io/webgon/

Các đường dẫn tài nguyên là tương đối, hỗ trợ triển khai trong thư mục `/webgon/`. Với hosting tĩnh khác, chọn thư mục xuất bản là `dist`, không cần lệnh build.

## Chức năng và giới hạn

- Giao diện sáng/tối, responsive, hiệu ứng hỗ trợ giảm chuyển động.
- Bảng giá, phần ước tính phí ban đầu và hàng tháng.
- Tải hoặc sao chép yêu cầu báo giá.
- Nội dung AI là minh họa; chưa gọi mô hình hoặc API.
- Biểu mẫu chưa gửi đến máy chủ; dữ liệu chỉ xử lý trong trình duyệt.
- Giá là tham khảo; cần xác nhận trước khi kinh doanh.
- Font Google được tải từ dịch vụ bên ngoài.

## Cấu trúc

- `dist/`: tài nguyên website sẵn sàng triển khai.
- `verify-pricing.cjs`: kiểm tra các trường hợp tính giá.
- `.github/workflows/deploy.yml`: kiểm tra và triển khai GitHub Pages.

Không lưu khóa API hoặc token trong mã nguồn. Nếu thêm AI thật, hãy gọi nhà cung cấp qua backend có quản lý bí mật và hạn mức.
