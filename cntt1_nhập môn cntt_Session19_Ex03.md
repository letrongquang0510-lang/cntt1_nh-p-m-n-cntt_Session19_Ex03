# **Yêu cầu đầu ra**

## Input (Mã dự phòng), Process (Xác thực/Hủy mã cũ/Cấp mã mới), Output (Hệ thống an toàn).

- Input (Đầu vào) : Mật khẩu tài khoản AWS + 1 mã Backup Code hợp lệ (lưu trữ ngoài điện thoại).
  
- Process (Xác thực / Hủy mã cũ / Cấp mã mới) :

1. Xác thực : Đăng nhập AWS bằng mật khẩu và mã Backup Code.
 
2. Hủy mã cũ : Vào IAM xoá liên kết thiết bị MFA trên điện thoại đã mất.
 
3. Cấp mã mới : Đăng ký MFA trên thiết bị mới và tạo bộ Backup Codes mới (vô hiệu hoá bộ cũ).

- Output (Hệ thống an toàn) : Khôi phục quyền truy cập thành công, chặn hoàn toàn nguy cơ truy cập từ điện thoại cũ.

## Giải thích tại sao không được lưu Backup Codes dưới dạng ảnh trong thư viện điện thoại.

- Lý do không lưu Backup Codes dạng ảnh trong điện thoại.

1. Mất tác dụng 2FA : Người nhặt được điện thoại nếu mở được khóa máy sẽ lấy được cả MFA lẫn Backup Code trên cùng một thiết bị.
2. Rò rỉ qua Cloud : Ảnh dễ bị đồng bộ lên Google Photos/iCloud, nguy cơ rò rỉ khi tài khoản cá nhân bị bẻ khóa.
3. Thiếu mã hóa : Mã độc hoặc ứng dụng có quyền truy cập thư viện ảnh có thể quét OCR để lấy trộm mã tự động.
