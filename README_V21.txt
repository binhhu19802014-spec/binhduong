V21 - MÁY PHỤ KHÔNG CẦN BIẾT/ NHẬP MẬT KHẨU MÁY CHÍNH

Cơ chế mới
-----------
MÁY CHÍNH:
- Vẫn đăng nhập Firebase bằng binhhu19802014@gmail.com.
- Duyệt máy phụ và cấp từng tuyến.

MÁY PHỤ / ĐIỆN THOẠI:
- Không có ô mật khẩu máy chính.
- Phần mềm tự tạo một tài khoản Firebase thiết bị riêng trong nền bằng Email/Password.
- Mật khẩu tài khoản thiết bị được tạo ngẫu nhiên và chỉ lưu trên chính trình duyệt máy phụ.
- Tự tạo Mã thiết bị.
- Tự gửi yêu cầu lên deviceRequests/<Firebase UID của máy phụ>.
- Sau khi máy chính duyệt, máy phụ tự nhận quyền và tải các tuyến được giao.
- Không cần biết mật khẩu binhhu19802014@gmail.com.

AN TOÀN DỮ LIỆU
----------------
- 42 tuyến gốc không thay đổi.
- Cấp/thu hồi quyền không ghi đè state/main.
- Máy phụ chỉ được dùng sau khi UID tài khoản thiết bị nằm trong authorizedUids.
- Máy phụ vẫn chỉ merge đúng tuyến được cấp bằng transaction của V19/V20.
- Ảnh hiện trạng và chiều cao mương giữ nguyên.
- Sửa/cập nhật 1 lần -> routeLocks/surveyLocks khóa lại.
- Máy chính mở lại 1 lần khi cần.

BẮT BUỘC LÀM 1 LẦN TRÊN FIREBASE
---------------------------------
V21 dùng tài khoản Firebase riêng cho từng thiết bị, nên cần cập nhật Firestore Rules:
1. Firebase Console -> Firestore -> Rules.
2. Mở file firestore.rules trong gói V21.
3. Copy toàn bộ nội dung -> dán thay rules hiện tại -> Publish.

KHÔNG cần bật Phone OTP.
KHÔNG cần bật Anonymous Authentication.
Email/Password đang dùng cho tài khoản chính cũng được V21 dùng để tự tạo tài khoản thiết bị nền.

Triển khai web:
- Upload toàn bộ file V21 lên GitHub main.
- Chờ Vercel Ready/Production.
- Ctrl+Shift+R trên máy tính; trên điện thoại đóng tab cũ rồi mở lại URL.
