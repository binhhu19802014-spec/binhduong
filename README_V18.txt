V18 - MÁY CHÍNH CỐ ĐỊNH THEO DEVICE ID

Máy chính:
e5bd6766-c82f-4440-a0d0-fd2887dfce08

Nguyên tắc:
1. Nếu deviceId hiện tại đúng mã trên -> nhận MÁY CHÍNH ngay khi mở app.
2. Không cần Workspace, Firebase hoặc Internet để:
   - nhìn thấy đủ 42 tuyến;
   - Sửa tuyến;
   - cập nhật tuyến không giới hạn.
3. Nút CẤP TUYẾN vẫn luôn hiện ở máy chính.
4. Muốn cấp tuyến thực tế cho máy phụ thì cần Cloud vì phải tải danh sách máy phụ.
5. Workspace mặc định tự điền: CUALO-2026.
6. Nếu ô Workspace bị trống, cloudConnect() tự điền lại trước khi kiểm tra.
7. Máy phụ vẫn phụ thuộc:
   - authorizedDevices;
   - routeAssignments;
   - routeLocks / surveyLocks.
8. Giữ nguyên:
   - 42 tuyến bắt buộc;
   - dữ liệu khảo sát;
   - chiều cao mương;
   - ảnh hiện trạng;
   - khóa sửa 1 lần của máy phụ.

Triển khai:
Upload toàn bộ file lên GitHub main -> Vercel Ready/Production -> Ctrl+Shift+R.
