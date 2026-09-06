V36 - SỬA XÓA DỮ LIỆU KHẢO SÁT TRÊN MÁY CHỦ

Đã sửa nút Xóa trong bảng Dữ liệu khảo sát:

- Chỉ máy chủ được xóa.
- Xóa trực tiếp bản ghi của idTuyen khỏi Firestore state/main.data.
- Xóa ảnh tương ứng trong workspaces/{ws}/photos/{routeId}.
- Xóa surveyLocks và routeLocks của tuyến để có thể nhập lại ngay.
- KHÔNG xóa tuyến khỏi Quản lý tuyến.
- Sau khi xóa, máy chủ đọc lại Cloud nên dữ liệu cũ không xuất hiện lại.
- Sau đó có thể chọn đúng tuyến và nhập lại số liệu khảo sát mới.

Nút trên máy chủ đổi thành “Xóa dữ liệu” để phân biệt với “Xóa tuyến” trong Quản lý tuyến.
