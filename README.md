# Github-guide

## Cách chỉ lấy 1 Folder trong 1 dự án lớn

Cách 1: 
git clone --no-checkout url (link)
cd python_lab
git sparse-checkout init --cone
git sparse-checkout set demoSQLInjection
git checkout main

Lợi ích:

Chỉ lấy thư mục demoSQLInjection.
Giữ nguyên lịch sử commit của thư mục đó.


Cách 2:
svn checkout url (link) + folder muốn tải --depth infinity

Lợi ích: Chỉ tải thư mục demoSQLInjection, không cần clone toàn bộ repo.


## Cách thay đổi tài khoản github khi bị báo lỗi 
"
remote: Permission to example_name_1/example_s.git denied to example_name_2.
fatal: unable to access 'https://github.com/example_name_1/example_s.git/': The requested URL returned error: 403
"

+ example_name_1 ở tài khoản 1
+ example_name_2 ở tài khoản 2

+ Steps: (in window)

B1. Xóa thông tin GitHub khỏi Credential Manager (Windows)
Mở Control Panel → Credential Manager.
Chọn Windows Credentials hoặc Generic Credentials.
Tìm github.com, nhấn Remove để xóa thông tin cũ.

B2. Xác thực lại khi push code Sau khi xóa, thử git push lại. Nếu Git yêu cầu đăng nhập, hãy nhập:
Username: <user_name> (Tài khoản mà bạn muốn dùng)
Password: Personal Access Token (PAT) (không phải mật khẩu GitHub).

