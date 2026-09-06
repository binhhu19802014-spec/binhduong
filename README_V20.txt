V20 - ĐỒNG BỘ QUYỀN MÁY PHỤ

- Sau khi máy chính cấp quyền, máy phụ tự tải lại config/meta mỗi 5 giây.
- Máy phụ tự đồng bộ khi quay lại tab/cửa sổ.
- Có nút "Đồng bộ quyền ngay" trong Cloud.
- Khi Cloud xác nhận authorizedDevices, phần mềm cache quyền theo đúng Workspace + deviceId.
- Cache gồm danh sách tuyến được cấp và trạng thái khóa của các tuyến đó.
- Nếu mới được cấp quyền thiết bị nhưng chưa cấp tuyến, bảng hiển thị:
  "Đã cấp quyền máy • Chưa cấp tuyến".
- Khi máy chính cấp tuyến, máy phụ tự nhận tuyến qua snapshot/polling.
- Cache chỉ là dự phòng; khi Cloud tải được meta mới thì quyền/thu hồi quyền được cập nhật lại.
- Giữ nguyên V19: máy phụ không full-state push; chỉ merge đúng tuyến bằng Firestore transaction; không làm mất dữ liệu máy khác.
