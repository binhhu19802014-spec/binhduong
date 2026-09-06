V14 - KHỞI TẠO 42 TUYẾN TRƯỚC LOCAL/CLOUD

Sửa lỗi gốc V13:
- Khôi phục hàm $() lấy phần tử DOM đã bị mất khi bỏ màn hình đăng nhập.
- Lỗi này từng làm JavaScript dừng trước khi render nên Quản lý tuyến hiện 0.

Cấu trúc V14:
1. Ngay khi JavaScript khởi tạo: routes = 42 tuyến gốc.
2. Sau đó mới đọc Local và merge lên 42 tuyến.
3. Sau đó mới đọc Firestore và merge lên 42 tuyến.
4. Cloud routes=[] bị bỏ qua, không thể xóa 42 tuyến.
5. Quản lý tuyến luôn có tối thiểu 42 tuyến ngay cả khi chưa kết nối Cloud.
6. Chỉ máy chính được ghi bản phục hồi danh mục lên Firestore.
7. Giữ phân quyền máy chính/máy phụ, cấp tuyến, sửa 1 lần rồi khóa.
8. Không thay đổi/xóa dữ liệu khảo sát; chiều cao mương và ảnh hiện trạng vẫn giữ cơ chế Cloud V11-V13.
9. 42 tuyến gốc không thể xóa; máy chính vẫn được sửa nội dung tuyến không giới hạn.

TRIỂN KHAI:
Upload toàn bộ file lên GitHub main -> chờ Vercel Ready/Production -> mở website và Ctrl+Shift+R.
