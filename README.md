# Github-guide

# Cách chỉ lấy 1 Folder trong 1 dự án lớn

Cách 1: 
git clone --no-checkout https://github.com/ArthurNguyen40/python_lab.git
cd python_lab
git sparse-checkout init --cone
git sparse-checkout set demoSQLInjection
git checkout main

Lợi ích:

Chỉ lấy thư mục demoSQLInjection.
Giữ nguyên lịch sử commit của thư mục đó.


Cách 2:
svn checkout https://github.com/ArthurNguyen40/python_lab/trunk/demoSQLInjection --depth infinity

Lợi ích: Chỉ tải thư mục demoSQLInjection, không cần clone toàn bộ repo.
