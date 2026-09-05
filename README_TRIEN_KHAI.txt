BỘ TRIỂN KHAI CLOUD - KHẢO SÁT MƯƠNG CỬA LÒ

1) FIREBASE
- Tạo Firebase Project.
- Authentication > Sign-in method > bật Email/Password.
- Firestore Database > Create database.
- Project settings > Your apps > Web app > lấy firebaseConfig.
- Mở firebase-config.js và thay 6 chuỗi __...__ bằng giá trị thật.
- Firestore > Rules > dán toàn bộ nội dung firestore.rules > Publish.
- Authentication > Settings > Authorized domains: sau khi deploy Vercel, thêm tên miền *.vercel.app hoặc domain riêng nếu Firebase chưa tự nhận.

2) VERCEL
- Upload/deploy nguyên thư mục này lên Vercel.
- Sau deploy sẽ có URL HTTPS, ví dụ https://ten-phan-mem.vercel.app.
- Mở URL này trên PC/iPhone/Samsung.

3) DÙNG NHIỀU MÁY
- Quản trị mở Cloud, đăng ký tài khoản Firebase bằng email, dùng Workspace CUALO-2026 và Kết nối.
- Tài khoản đầu tiên tạo Workspace là chủ.
- Chủ nhập email cán bộ tại mục Cấp quyền.
- Cán bộ đăng ký/đăng nhập Cloud bằng đúng email đã được cấp và kết nối cùng Workspace.
- Dữ liệu sẽ đồng bộ Firestore giữa các thiết bị.

4) ĐIỆN THOẠI
- iPhone: Safari > Share > Add to Home Screen.
- Samsung/Android: Chrome > menu > Add to Home screen / Install app.

LƯU Ý: firebase-config.js không chứa mật khẩu; Firebase Web API key không phải secret. Bảo mật dữ liệu dựa vào Authentication + Firestore Security Rules.
