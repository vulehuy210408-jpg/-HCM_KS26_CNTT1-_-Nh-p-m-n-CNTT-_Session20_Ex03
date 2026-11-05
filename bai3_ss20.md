# Bài 3 : Quản lý rủi ro khi mất thiết bị xác thực

**Báo cáo phân tích (IPO)**

- Input (Mã dự phòng), Process (Xác thực/Hủy mã cũ/Cấp mã mới), Output (Hệ thống an toàn).

  - **Input**: Mã dự phòng bộ mã dùng cho các trường hợp khẩn cấp thường là những kí tự ngẫu nhiên do hệ thống AWS cung cấp và người dùng lưu trữ an toàn khi cài đặt 2FA lần đầu tiên. Xấc thực phụ Email quản trị, số điện thoại 
  - **Process**: Sử dụng mật mã dự phòng để đăng nhập gấp. Truy cập vào trang AWS và nhập tài khoản. Sau đó nhập trong các mã dự phòng chưa từng sử dụng.Sau khi đăng nhập thành công vào AWS thì vào phần trung tâm tài khoản và vô hiệu hóa các mã độc hại từ thiết bị cũ. Cấp phát thiết bị xác thực mới, cài đặt ứng dụng gg Authenticator trên thiết bị mới và quét mã QR để tạo mâ mới cho tài khoản lưu lại toàn bộ mã. 
  - **Output**: Khôi phục quyền truy cập quản trị AWS cho Lead Developer, vô hiệu hóa hoàn toàn nguy cơ kẻ gian lợi dụng thiết bị cũ để xâm nhập vào tài nguyên đám mây
  - Giải thích tại sao không được lưu Backup Codes dưới dạng ảnh trong thư viện điện thoại vì: Nguy cơ từ mã độc hại ứng dụng nhiều ứng dụng có quyền truy cập vào bộ sưu tập trong máy của mình và thư viện ảnh thường tự động sao lưu lên GG Phótos hoặc Icloud. Trường hợp cuối là nếu điện thoại bị mất hoặc ai mượn lỡ người ta vào bộ sưu tập thì chúng ta sẽ bị lộ mật khẩu.
  