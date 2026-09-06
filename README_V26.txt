V26 - SỬA CHỨC NĂNG LƯU TUYẾN MỚI

- Trong Quản lý tuyến có nút riêng: LƯU TUYẾN MỚI.
- + Thêm tuyến mới -> mã tự tăng -> nhập thông tin -> LƯU TUYẾN MỚI.
- Lưu local trước.
- Nếu Cloud đang kết nối, dùng Firestore transaction để APPEND tuyến mới vào state/main.routes.
- Không ghi đè dữ liệu khảo sát.
- Sau khi Cloud lưu thành công, đọc lại state/main và cập nhật ngay danh mục trên máy chính.
- Các máy khác nhận tuyến mới qua realtime snapshot.
- Nếu tích cấp cho TẤT CẢ máy, tuyến mới được giao cho toàn bộ máy phụ sau khi lưu.
- Khi sửa tuyến cũ, nút đổi thành Lưu cập nhật tuyến.
- 42 tuyến gốc vẫn được bảo vệ.
