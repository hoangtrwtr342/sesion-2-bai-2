1. Phân biệt Đường dẫn Tuyệt đối và Đường dẫn Tương đối
Đường dẫn Tuyệt đối (Absolute Path):
Bắt đầu từ thư mục gốc của ổ cứng (như C:\ trên Windows hoặc / trên macOS/Linux).
Chỉ rõ vị trí cố định trên một máy tính duy nhất. Mang sang máy khác rất dễ bị đứt gãy vì cấu hình thư mục khác nhau.
Đường dẫn Tương đối (Relative Path):
Bắt đầu từ vị trí của thư mục làm việc hiện tại (dùng . cho thư mục hiện tại và .. cho thư mục cha).
Giúp dự án có tính di động cao (Portability), các tệp luôn tìm thấy nhau dù dự án được chuyển sang máy tính hay hệ điều hành nào.


3. Khắc phục lỗi dự án của Bình
Phần 1: Nguyên nhân đường dẫn bị đứt gãy
Bình đã gắn cứng (hard-code) đường dẫn tuyệt đối phụ thuộc vào tài khoản cá nhân (C:\Users\Binh-K26\...).
Sang máy giáo viên, tên tài khoản đăng nhập khác (không có Binh-K26), hoặc bài tập được lưu ở ổ D:\, khiến hệ thống không tìm thấy đường dẫn trên và báo lỗi FileNotFoundError.


Phần 2: Sửa lại bằng Đường dẫn Tương đối (Relative Path)
Vì file code nằm trong Session-02, còn ảnh nằm trong thư mục con assets, ta dùng ký hiệu . (đại diện cho thư mục hiện tại) để trỏ đến ảnh:
Python

image_path = "./assets/logo.png"
