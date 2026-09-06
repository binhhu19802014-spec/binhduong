V27 - MÁY PHỤ HIỂN THỊ TUYẾN ĐƯỢC CẤP TRONG CẬP NHẬT KHẢO SÁT

Đã sửa:
1. Cập nhật khảo sát lấy danh sách tuyến trực tiếp từ:
   - danh mục routes đang đồng bộ Cloud;
   - config/meta.routeAssignments;
   - cache quyền cục bộ dự phòng khi mạng chậm.
2. Máy phụ hiển thị:
   - tuyến cấp riêng cho đúng máy đó;
   - tuyến cấp theo chế độ TẤT CẢ MÁY;
   - tuyến mới bổ sung nếu tuyến đó đã được cấp.
3. Khi máy chính cấp/thu hồi tuyến:
   - meta realtime cập nhật;
   - dropdown Cập nhật khảo sát tự làm mới.
4. Khi máy chính thêm tuyến mới:
   - state/main realtime cập nhật;
   - máy phụ nhận tuyến mới;
   - nếu tuyến đã cấp cho máy đó / ALL thì xuất hiện ngay trong dropdown.
5. Bổ sung nút “Đồng bộ danh sách tuyến” để máy phụ chủ động tải lại meta + state.
6. Có dòng trạng thái:
   - số tuyến đã đồng bộ;
   - chưa cấp quyền;
   - đã cấp quyền máy nhưng chưa cấp tuyến.
7. Giữ nguyên phân quyền:
   - máy phụ không thể cập nhật tuyến chưa được cấp;
   - khóa sau máy cập nhật đầu tiên vẫn giữ nguyên;
   - máy chính không giới hạn.
