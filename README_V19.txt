V19 - CẤP QUYỀN MÁY PHỤ KHÔNG LÀM MẤT DỮ LIỆU

- Sửa lỗi CLOUD_WS_STORE/CLOUD_CFG_STORE chưa khai báo.
- Máy phụ có thể gửi yêu cầu quyền; máy chính duyệt yêu cầu.
- Máy chính có thêm "Cấp quyền trực tiếp cho máy khác" bằng Mã thiết bị.
- Cấp/thu hồi quyền chỉ ghi config/meta, không chạm state/main.
- Sau khi cấp quyền, máy chính vào Quản lý tuyến để Cấp tuyến.

Chống mất dữ liệu:
- Máy chính được ghi toàn bộ state.
- Máy phụ không được full-state push.
- Máy phụ chỉ merge đúng tuyến được cấp bằng Firestore transaction.
- Dữ liệu các tuyến khác trên Cloud được giữ nguyên.
- Máy phụ phải tải xong state Cloud trước khi ghi.
- Khi Cloud tải xuống, record Cloud cùng tuyến là nguồn chuẩn; record local chưa có trên Cloud vẫn được giữ.
- Ảnh hiện trạng lưu riêng theo photos/<idTuyen>.
- Chiều cao mương tiếp tục đồng bộ trong record.

Máy chính: e5bd6766-c82f-4440-a0d0-fd2887dfce08
Workspace: CUALO-2026
