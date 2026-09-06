V38 - SỬA/XÓA TRỰC TIẾP TRONG DỮ LIỆU KHẢO SÁT

Đã kiểm tra lại theo ảnh thực tế của máy chủ.

XÓA:
- Chỉ cần hộp thoại Có/Không, không còn bắt nhập chữ XOA.
- Đọc state/main trực tiếp từ server.
- Chỉ update trường data để loại đúng idTuyen.
- Không phụ thuộc config/meta, routeLocks hay routeAssignments.
- Đọc lại server và xác minh bản ghi đã biến mất rồi mới báo thành công.
- Xóa ảnh và dọn khóa thực hiện riêng, lỗi các phần phụ không làm hỏng xóa số liệu.

SỬA:
- Máy chủ đọc dữ liệu hiện hành từ server.
- Ghi đè đúng idTuyen bằng update trường data.
- Đọc lại server xác minh sau cập nhật.
- Nếu Cloud không ghi được, không tiếp tục báo thành công.

Lưu ý:
- Máy chủ phải kết nối Cloud bằng tài khoản binhhu19802014@gmail.com vì Firestore Rules chỉ cấp quyền master cho tài khoản này.
- Giao diện có nhãn V38 để nhận biết đúng phiên bản.
