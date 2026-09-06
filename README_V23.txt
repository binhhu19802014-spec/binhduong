V23 - CẤP TUYẾN CHO TẤT CẢ MÁY + KHÓA SAU MÁY CẬP NHẬT ĐẦU TIÊN

CƠ CHẾ MỚI
----------
1. Máy chính vẫn có thể cấp quyền nhiều thiết bị cùng lúc như V22.
2. Trong Quản lý tuyến, mỗi tuyến có thêm:
   - tùy chọn "★ TẤT CẢ MÁY ĐÃ CẤP QUYỀN";
   - nút "Cấp tất cả máy".
3. Khi tuyến được cấp cho TẤT CẢ MÁY:
   - mọi máy phụ đã được cấp quyền đều thấy tuyến;
   - mọi máy đều có thể mở thao tác Sửa/Cập nhật;
   - máy nào LƯU/CẬP NHẬT thành công đầu tiên sẽ tạo khóa chung;
   - các máy phụ còn lại không thể cập nhật tuyến đó nữa.
4. Khóa chung áp dụng cho cả:
   - sửa thông tin tuyến trong Quản lý tuyến;
   - cập nhật dữ liệu khảo sát.
5. Máy chính:
   - sửa/cập nhật không giới hạn;
   - có thể bấm "Mở lại 1 lần";
   - sau khi mở lại, tất cả máy phụ được cấp tuyến lại có quyền thao tác;
   - máy nào cập nhật trước tiếp tục khóa tuyến cho các máy còn lại.

AN TOÀN DỮ LIỆU
----------------
- Cấp tuyến cho tất cả máy chỉ cập nhật routeAssignments + trạng thái khóa trong config/meta.
- Không xóa 42 tuyến.
- Không ghi đè dữ liệu khảo sát khi cấp quyền.
- Máy phụ vẫn chỉ merge đúng tuyến được cấp bằng transaction.
- Ảnh hiện trạng và chiều cao mương giữ nguyên.

GIỮ NGUYÊN V22/V21
------------------
- Máy phụ không cần mật khẩu máy chính.
- Máy chính cấp quyền nhiều máy cùng lúc.
- Máy chính đặt/đổi tên quản lý thiết bị.
- Tên quản lý mới dùng trong danh sách cấp tuyến và lịch sử khóa.
