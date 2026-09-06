V22 - CẤP QUYỀN NHIỀU MÁY + ĐỔI TÊN THIẾT BỊ

NÂNG CẤP QUẢN TRỊ THIẾT BỊ
---------------------------
1. Máy chính có thể cấp quyền nhiều máy cùng lúc:
   - Chọn từng máy bằng checkbox.
   - Có nút Chọn tất cả / Bỏ chọn.
   - Bấm "Cấp quyền các máy đã chọn".

2. Trước khi cấp, máy chính có thể đặt Tên quản lý riêng cho từng máy:
   Ví dụ:
   - Điện thoại Anh Hùng
   - Máy khảo sát 01
   - Máy đội thoát nước 2
   - iPhone tổ 3

3. Máy đã cấp quyền vẫn đổi tên được bất kỳ lúc nào:
   - Nhập tên mới tại "Tên quản lý thiết bị".
   - Bấm "Lưu tên".
   - Tên mới tự cập nhật vào routeAssignments để danh sách Cấp tuyến hiển thị đúng tên mới.

4. Cấp quyền nhiều máy / đổi tên:
   - CHỈ cập nhật config/meta và deviceRequests.
   - KHÔNG ghi đè state/main.
   - KHÔNG xóa 42 tuyến.
   - KHÔNG xóa dữ liệu khảo sát, ảnh hoặc chiều cao mương.

5. Giữ nguyên V21:
   - Máy phụ không cần mật khẩu máy chính.
   - Mỗi máy có Firebase UID riêng.
   - Máy chính duyệt quyền.
   - Sau đó máy chính Cấp tuyến.
   - Máy phụ sửa/cập nhật tuyến được giao đúng 1 lần rồi tự khóa.

LƯU Ý FIRESTORE RULES
---------------------
Giữ nguyên firestore.rules của V21/V22 và Publish 1 lần trên Firebase nếu chưa làm.

Triển khai:
- Upload toàn bộ file V22 lên GitHub main.
- Chờ Vercel Ready/Production.
- Máy tính: Ctrl+Shift+R.
- Điện thoại: đóng tab cũ, mở lại website.
