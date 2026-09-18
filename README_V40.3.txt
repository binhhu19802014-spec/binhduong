V40.3 - Google Maps FIX

- Giữ nguyên dữ liệu/cấu trúc V40.2.
- Không gọi Geocoding API.
- Nạp Maps JavaScript API theo loading=async, v=weekly.
- Chỉ khởi tạo Map sau khi container đã hiển thị và qua 2 frame render.
- Bổ sung gm_authFailure và trạng thái lỗi rõ hơn; nếu Google từ chối quyền, tự quay về bản đồ tham chiếu thay vì để vùng xám.
- Không thay localStorage keys của V40/V40 Bình đồ.

Lưu ý: nếu Console vẫn báo Permission Denied sau V40.3 thì đây là từ chối quyền phía Google Maps Platform/API project, không phải lỗi IntersectionObserver trong mã ứng dụng. Khi đó không cần tạo API key mới; cần xử lý quyền/billing Maps của project.
