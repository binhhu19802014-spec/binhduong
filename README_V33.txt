V33 - SỬA CHỨC NĂNG XÓA TUYẾN TRÊN MÁY CHỦ

Đã sửa:
- Máy chính xóa được các tuyến bổ sung/tuyến mới phát sinh.
- Xóa trực tiếp trên Firestore state/main.routes bằng transaction.
- Sau khi xóa, máy chính đọc lại Cloud nên tuyến không bị hiện lại.
- Xóa luôn:
  + routeAssignments của tuyến;
  + routeLocks của tuyến;
  + surveyLocks của tuyến.
- Các máy phụ nhận realtime và tuyến biến mất khỏi danh sách được cấp.

Bảo vệ dữ liệu:
- 42 tuyến gốc bắt buộc vẫn KHÔNG cho xóa.
- Dữ liệu khảo sát cũ của tuyến bổ sung được GIỮ LẠI để tránh mất số liệu.
- Ảnh khảo sát cũ cũng không bị xóa tự động.

Nếu muốn xóa luôn cả dữ liệu khảo sát + ảnh của tuyến, nên bổ sung thành một thao tác riêng có xác nhận mạnh để tránh xóa nhầm.
