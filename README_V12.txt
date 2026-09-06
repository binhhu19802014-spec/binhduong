V12 - 42 TUYẾN CLOUD + PHÂN QUYỀN THEO TUYẾN

- Tự đảm bảo danh mục có đủ 42 tuyến gốc.
- Nếu Cloud thiếu tuyến, máy chính tự bổ sung tuyến thiếu và ghi lại state/main.
- Máy chính: sửa/xóa/cập nhật tuyến không giới hạn.
- Máy chính có thể chọn một thiết bị đã được cấp quyền rồi bấm CẤP TUYẾN.
- Máy phụ chỉ thấy tuyến được cấp trong form khảo sát.
- Trong Quản lý tuyến, máy phụ chỉ sửa tuyến được cấp đúng 1 lần; sau khi lưu tuyến tự khóa.
- Máy chính có thể MỞ LẠI 1 LẦN hoặc cấp tuyến cho máy khác.
- Khảo sát cũng chỉ được cập nhật trên tuyến đã cấp; cơ chế khóa khảo sát 1 lần vẫn được giữ.
- Ảnh hiện trạng và Chiều cao mương tiếp tục đồng bộ Cloud theo V11.

TRIỂN KHAI:
1. Upload các file lên GitHub main.
2. Vercel tự deploy.
3. Mở website, Ctrl+Shift+R.
4. Trên máy chính: Cloud > Kết nối > Quản lý tuyến > chọn thiết bị > Cấp tuyến.
