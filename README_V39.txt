V39 - SỬA LỖI KHÔNG GIỮ SỐ LIỆU KHI CẬP NHẬT KHẢO SÁT

Nguyên nhân:
- refreshRouteSelect() luôn gọi loadRoute().
- Đồng bộ Cloud/realtime/polling gọi refreshRouteSelect().
- Vì vậy trong lúc người dùng đang sửa số liệu, form có thể bị nạp lại bản ghi cũ trước khi bấm Lưu.

Đã sửa:
- Thêm trạng thái surveyFormDirty.
- Khi người dùng thay đổi bất kỳ ô khảo sát nào, form chuyển sang trạng thái đang chỉnh sửa.
- Đồng bộ Cloud vẫn cập nhật bảng/KPI nhưng KHÔNG được nạp lại các ô form đang nhập.
- Chỉ đổi tuyến, Hủy sửa hoặc Lưu thành công mới cho phép nạp lại form.
- Sửa ảnh/xóa ảnh cũng đánh dấu form đang chỉnh sửa.
- Sau Lưu thành công, form đọc lại dữ liệu Cloud mới nhất và hiển thị đúng số liệu vừa cập nhật.
