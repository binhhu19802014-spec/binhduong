V16 - RENDER 42 TUYẾN TRƯỚC, PHÂN QUYỀN SAU

Cấu trúc:
1. renderRouteTable() chỉ dựng dữ liệu 42 tuyến, KHÔNG gọi Firebase/phân quyền khi tạo dòng.
2. Sau khi 42 dòng đã xuất hiện, updateRouteActionCells() mới gắn:
   - Máy chính: Sửa, Cấp tuyến, Thu hồi, Mở lại 1 lần.
   - Máy phụ: Sửa 1 lần / Đã khóa / Không được cấp tuyến.
3. Nếu Cloud/phân quyền lỗi, bảng vẫn giữ 42 dòng; chỉ cột Thao tác hiện "Chưa tải quyền".
4. Có fallback cuối cùng dựng trực tiếp cloneBaseRoutes() nếu render chính gặp lỗi.
5. Giữ nguyên:
   - 42 tuyến gốc bắt buộc;
   - Local/Cloud chỉ merge, không được routes=[] ghi đè;
   - máy chính sửa không giới hạn;
   - máy phụ chỉ sửa tuyến được cấp 1 lần rồi khóa;
   - dữ liệu khảo sát, chiều cao mương, ảnh hiện trạng và đồng bộ Cloud.

Triển khai:
Upload toàn bộ file lên GitHub main -> Vercel Ready/Production -> Ctrl+Shift+R.
