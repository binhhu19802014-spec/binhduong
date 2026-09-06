V11 - DONG BO ANH + CHIEU CAO
1. Khi bấm Lưu/Cập nhật:
   - state/main được cập nhật ngay, gồm trường cao (Chiều cao mương).
   - ảnh được lưu riêng tại workspaces/<workspace>/photos/<idTuyen>.
2. Máy khác:
   - giữ cache ảnh Cloud độc lập, nên ảnh về trước hay dữ liệu về trước đều ghép đúng.
3. Ảnh được nén xuống mức an toàn để tránh vượt giới hạn document Firestore.
4. Upload toàn bộ file trong ZIP lên GitHub main, Vercel sẽ tự deploy.
