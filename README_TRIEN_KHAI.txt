BỘ PHẦN MỀM KHẢO SÁT MƯƠNG CỬA LÒ
PHIÊN BẢN: 1 TÀI KHOẢN FIREBASE + PHÂN QUYỀN THIẾT BỊ + KHÓA TUYẾN 1 LẦN

1. TÀI KHOẢN DÙNG CHUNG
- Phần mềm KHÔNG còn màn hình đăng nhập/đăng ký cục bộ.
- Firebase chỉ dùng tài khoản: binhhu19802014@gmail.com.
- Mỗi máy có một Mã thiết bị riêng lưu trên trình duyệt.

2. MÁY CHÍNH
- Kết nối Cloud bằng tài khoản binhhu19802014@gmail.com.
- Lần đầu phần mềm hỏi có đặt thiết bị này làm MÁY CHÍNH hay không: chọn Đồng ý trên đúng máy quản trị.
- Máy chính được thêm/sửa/xóa tuyến không giới hạn.
- Máy chính duyệt/thu hồi quyền thiết bị khác.
- Máy chính có thể mở khóa từng tuyến để thiết bị phụ được sửa đúng 1 lần tiếp theo.

3. MÁY PHỤ
- Kết nối Cloud bằng cùng tài khoản Firebase dùng chung.
- Phần mềm tự gửi yêu cầu cấp quyền theo Mã thiết bị.
- Sau khi máy chính duyệt, máy phụ được sử dụng phần mềm.
- Trong Quản lý tuyến: chỉ có nút Sửa, không có Xóa.
- Một tuyến chỉ được máy phụ sửa/cập nhật đúng 1 lần; sau khi lưu, tuyến tự khóa với mọi máy phụ.
- Tuyến đã khóa chỉ máy chính mở lại.

4. CHIỀU CAO MƯƠNG
- Form Cập nhật khảo sát đã thêm trường Chiều cao mương (m).
- Dữ liệu khảo sát và file Excel xuất ra đều có chiều cao mương.

5. FIREBASE
- Authentication > Sign-in method > Email/Password phải bật.
- Không cần Phone/OTP.
- Dán nội dung firestore.rules của gói này vào Firestore > Rules > Publish.
- firebase-config.js đã chứa cấu hình dự án khao-sat-muong-cua-lo.

6. TRIỂN KHAI VERCEL
- Upload các file trong gói này lên repo GitHub đang kết nối với Vercel.
- Commit và chờ Vercel Deployment = Ready.
- Mở website và Ctrl+F5 để nhận bản mới.

LƯU Ý BẢO MẬT
- Do tất cả thiết bị dùng cùng một Firebase account, phân quyền theo thiết bị/khóa tuyến được phần mềm thực thi ở tầng ứng dụng.
- Nếu cần ngăn tuyệt đối việc một thiết bị cố tình sửa dữ liệu bằng công cụ lập trình, phải chuyển sang mỗi người/mỗi thiết bị một tài khoản Firebase hoặc có backend cấp token riêng.
