V24 - TẤT CẢ MÁY DÙNG CHUNG MỘT SỐ LIỆU CLOUD

MỤC TIÊU
--------
- Máy phụ A cập nhật tuyến -> máy chính tự nhận số liệu mới.
- Máy phụ B/C/... đã được cấp quyền -> tự nhận cùng số liệu mới.
- Máy chính cập nhật -> tất cả máy phụ tự nhận số liệu mới.
- Không cần nhập lại hoặc tải file thủ công.

CƠ CHẾ ĐỒNG BỘ
--------------
1. state/main trên Firestore là nguồn dữ liệu chung.
2. Mọi máy đã được cấp quyền đều có onSnapshot theo dõi state/main.
3. Khi có cập nhật:
   - chỉ merge đúng id tuyến đang sửa bằng Firestore transaction;
   - updatedAt + updatedBy được ghi lên Cloud;
   - sau commit, máy thao tác đọc lại Cloud;
   - các máy khác nhận snapshot và render lại ngay.
4. Nếu cùng idTuyen đã có trên Cloud:
   - Cloud là nguồn chuẩn;
   - local cũ không được ghi đè Cloud.
5. Bản local chưa từng có trên Cloud vẫn được giữ tạm với localPending=true để tránh mất dữ liệu cũ.

CHỐNG GHI ĐÈ
------------
- Máy chính KHÔNG còn full-state push khi sửa thông thường.
- Máy phụ KHÔNG bao giờ full-state push.
- Save khảo sát/sửa tuyến của cả máy chính và máy phụ đều merge đúng tuyến.
- Full-state chỉ còn cho khởi tạo Cloud đặc biệt; phục hồi 42 tuyến dùng merge:true và không đụng data khảo sát.
- Settings của máy chính merge riêng, không ghi đè data.

GIỮ NGUYÊN V23
--------------
- Có thể cấp tuyến cho TẤT CẢ MÁY.
- Tất cả máy phụ được thao tác tuyến đó cho tới khi một máy cập nhật trước.
- Máy cập nhật đầu tiên tạo khóa chung cho toàn bộ máy phụ còn lại.
- Máy chính sửa không giới hạn và có thể Mở lại 1 lần.
- Máy phụ không cần mật khẩu máy chính.
- Cấp quyền nhiều máy và đổi tên thiết bị.
- 42 tuyến, ảnh hiện trạng, chiều cao mương giữ nguyên.

TRIỂN KHAI
----------
Upload toàn bộ V24 lên GitHub main -> Vercel Ready/Production.
Máy tính Ctrl+Shift+R; điện thoại đóng tab cũ rồi mở lại URL.
