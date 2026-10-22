# Multi-Restaurant Food Delivery

README này mô tả cấu trúc thư mục và quy ước đặt file của dự án. Các thư mục hiện tại là bộ khung để tổ chức mã nguồn; hãy đặt file vào đúng nơi theo trách nhiệm thay vì gom mọi thứ vào một thư mục.

## Cấu trúc thư mục

```text
.
├── api/          # Điểm vào API, route/endpoint và xử lý request
├── asset/        # Tài nguyên tĩnh: ảnh, biểu tượng, font, CSS/JS dùng chung
├── controls/     # Thành phần giao diện có thể tái sử dụng
├── database/     # Kết nối, khởi tạo schema, migration và truy vấn mức cơ sở dữ liệu
├── docs/         # Tài liệu thiết kế, hướng dẫn và ghi chú kỹ thuật
├── forms/        # Biểu mẫu và logic kiểm tra dữ liệu đầu vào
├── includes/     # Thành phần hoặc cấu hình dùng chung được nạp ở nhiều nơi
├── models/       # Mô hình dữ liệu và quy tắc nghiệp vụ gắn với dữ liệu
├── n8n/          # Workflow và cấu hình tích hợp dành cho n8n
├── properties/   # Tệp cấu hình thuộc tính theo môi trường hoặc chức năng
├── scripts/      # Script hỗ trợ phát triển, kiểm tra, triển khai hoặc bảo trì
├── services/     # Logic nghiệp vụ và tích hợp với dịch vụ bên ngoài
└── utilities/    # Hàm tiện ích dùng chung, không gắn với một tính năng cụ thể
```

## Cách sử dụng

- **API mới:** đặt endpoint trong `api/`; chuyển xử lý nghiệp vụ sang `services/` và truy cập dữ liệu qua `models/` hoặc lớp phù hợp trong `database/`.
- **Màn hình hoặc thành phần giao diện:** đặt thành phần dùng lại trong `controls/`, biểu mẫu trong `forms/`, và tài nguyên tĩnh trong `asset/`.
- **Tích hợp hoặc tự động hóa:** đặt logic tích hợp trong `services/`; workflow n8n và tài liệu liên quan trong `n8n/` và `docs/`.
- **Mã dùng chung:** đặt cấu hình include trong `includes/`, cấu hình thuộc tính trong `properties/`, và hàm tổng quát trong `utilities/`.
- **Tài liệu và công cụ:** ghi hướng dẫn trong `docs/`; đặt script hỗ trợ trong `scripts/`.

Khi thêm tính năng, hãy giữ phần giao tiếp, nghiệp vụ, dữ liệu và giao diện tách biệt; tái sử dụng mã có sẵn thay vì sao chép. Nếu một thư mục phát triển thành nhiều phần, có thể tạo thư mục con theo tính năng, ví dụ `api/orders/` hoặc `services/payments/`.

## Lệnh chạy dự án

