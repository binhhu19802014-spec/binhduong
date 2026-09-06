V17 - MÁY CHÍNH ĐỘC LẬP TRƯỚC FIREBASE

- Máy chính được lưu marker cục bộ theo đúng deviceId.
- Sau khi xác nhận một lần với workspace, máy chính được nhận diện trước khi cloudMeta tải.
- Máy chính luôn nhìn thấy SỬA + CẤP TUYẾN.
- Nếu danh sách máy phụ chưa tải, nút CẤP TUYẾN vẫn hiện và hướng dẫn mở Cloud để tải danh sách.
- Firestore ownerDeviceId dùng để đối chiếu marker:
  + trùng deviceId -> củng cố marker;
  + khác deviceId -> xóa marker cũ để tránh nhận nhầm.
- Máy phụ không có marker nên vẫn phụ thuộc authorizedDevices + routeAssignments + routeLocks.
- Giữ nguyên 42 tuyến, dữ liệu khảo sát, ảnh hiện trạng.
- Sửa normalizeSurveyRow để giữ trường cao/Chiều cao mương khi đọc Local/Cloud.

LẦN ĐẦU SAU KHI NÂNG V17:
Trên đúng máy chính hiện tại, vào Cloud -> Kết nối một lần.
Sau khi V17 đối chiếu ownerDeviceId thành công, marker máy chính được lưu trên trình duyệt.
Từ lần mở sau, máy chính được nhận diện ngay cả khi dữ liệu phân quyền Firebase chưa tải.

Triển khai: upload toàn bộ file lên GitHub main -> Vercel Ready/Production -> Ctrl+Shift+R.
