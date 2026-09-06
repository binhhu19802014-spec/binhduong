V37 - KIỂM TRA VÀ SỬA TRIỆT ĐỂ QUYỀN SỬA/XÓA DỮ LIỆU KHẢO SÁT CỦA MÁY CHỦ

Nguyên nhân được xử lý:
1. Trước đây trình duyệt có thể được nhận là “máy chủ” theo local/device marker nhưng phiên Firebase đang dùng không phải tài khoản chính. Giao diện cho phép bấm, nhưng Firestore Rules có thể từ chối ghi/xóa.
2. Xóa V36 gộp xóa state và dọn lock trong cùng luồng. Lỗi quyền/config meta có thể làm cả thao tác xóa số liệu thất bại.
3. Snapshot realtime có thể cập nhật giao diện trong lúc thao tác quản trị đang commit.

V37:
- Sửa/xóa dữ liệu trên máy chủ bắt buộc phiên Cloud thực tế là binhhu19802014@gmail.com.
- Nếu chưa đúng phiên, phần mềm báo rõ phải KẾT NỐI CLOUD; không giả báo đã lưu.
- Sửa dùng transaction ghi đè đúng idTuyen.
- Xóa state/main.data là thao tác chính, độc lập với xóa ảnh/dọn khóa.
- Sau xóa, đọc trực tiếp từ server và kiểm tra idTuyen đã biến mất.
- Tạm bỏ qua snapshot realtime trong lúc máy chủ đang sửa/xóa để tránh dữ liệu cũ chen vào.
- Ảnh và khóa được dọn riêng theo kiểu best-effort.
- Danh mục tuyến vẫn giữ nguyên để có thể nhập lại.
- Có nhãn V37 trên giao diện để kiểm tra đúng bản đang chạy.
