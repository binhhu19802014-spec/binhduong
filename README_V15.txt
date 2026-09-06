V15 - SỬA BẢNG 42 TUYẾN BỊ TRẮNG

Nguyên nhân V14:
- routes đã có đủ 42 tuyến nên bộ đếm hiện 42.
- Nhưng các hàm tiện ích safeParse(), escapeHtml(), today(), formatDateVN(), money()
  bị mất khi bỏ khối đăng nhập cũ.
- renderRouteTable() gọi escapeHtml() nên JavaScript dừng khi tạo dòng đầu tiên.

V15:
1. Khôi phục đầy đủ các hàm tiện ích dùng chung.
2. 42 tuyến khởi tạo trước Local/Cloud như V14.
3. Mỗi dòng Quản lý tuyến có cơ chế fallback: một lỗi quyền/Cloud không thể làm trắng cả bảng.
4. Chưa kết nối Cloud vẫn phải nhìn thấy đủ 42 tuyến.
5. Giữ nguyên:
   - máy chính sửa không giới hạn;
   - máy phụ chỉ sửa tuyến được cấp 1 lần rồi khóa;
   - máy chính mở lại/cấp lại;
   - dữ liệu khảo sát không bị xóa;
   - chiều cao mương và ảnh hiện trạng tiếp tục đồng bộ Cloud.

Triển khai: upload toàn bộ file lên GitHub main -> Vercel Ready/Production -> Ctrl+Shift+R.
