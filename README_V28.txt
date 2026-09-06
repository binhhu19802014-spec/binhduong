V28 - SỬA DỨT ĐIỂM SỐ LIỆU CÁC MÁY KHÔNG KHỚP

Nguyên nhân đã sửa:
1. Listener Firestore cũ bỏ qua snapshot nếu cloudApplying=true. Một cập nhật từ máy khác có thể bị bỏ qua.
2. Bản cũ còn ghép các bản ghi local riêng vào data Cloud, nên máy A có thể 4 tuyến nhưng máy B có 7 tuyến.
3. Thay đổi đơn giá có thể chỉ tính lại local, làm Tổng dự toán khác nhau.

Cơ chế V28:
- Khi đã kết nối và được cấp quyền, state/main Cloud là nguồn dữ liệu DUY NHẤT.
- Không ghép thêm bản khảo sát local riêng vào số liệu Cloud.
- Không bỏ qua snapshot realtime.
- Mỗi 10 giây tự kiểm tra lại state/main từ server.
- Khi app lấy lại focus / mở lại tab, tự tải state Cloud mới nhất.
- Có nút “↻ Đồng bộ số liệu chung”.
- Sau mỗi lần lưu khảo sát, máy lưu đọc lại server để xác nhận bản chung.
- Máy chính đổi đơn giá sẽ tính lại toàn bộ dự toán Cloud; mọi máy tự nhận cùng đơn giá và tổng dự toán.
- Máy phụ không tạo đơn giá riêng khi đang dùng Cloud.
- Tuyến mới, phân quyền, khóa máy cập nhật đầu tiên và ảnh vẫn giữ nguyên.

Kết quả mong đợi:
Nếu Cloud đang có 7 bản khảo sát thì máy chính và mọi máy phụ được cấp quyền đều phải hiện 7/... và cùng Tổng chiều dài, Tổng bùn, Tổng hố thu, Tổng dự toán sau khi đồng bộ.
