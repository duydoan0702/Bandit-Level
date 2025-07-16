
# Bandit Level

## 🧩 Challenge: Level 18

### 📝 Description
Mật khẩu cho cấp độ tiếp theo được lưu trong tệp readme trong thư mục home. Thật không may, ai đó đã sửa đổi `.bashrc` để đăng xuất bạn khi bạn đăng nhập bằng SSH.

> Link: https://overthewire.org/wargames/bandit/bandit19.html

---

## 🧠 Chiến lược giải
- Tìm cách truy cập mà không chạy file `.brshrc` để tránh bị đăng xuất khi vừa mới đăng nhập.
---

## 🛠️ Cách giải

1. Dùng `ssh` đề thực hiện đăng nhập trực tiếp và chạy file `readme`

```
ssh bandit18@bandit.labs.overthewire.org -p 2220 "cat /home/bandit18/readme"
```
- sau ghi chạy lệnh sau sẽ nhận được passowrd


---

## 🏁 Password

```
cGWpMaKXVwDUNgPAVJbWYuGHVn9zl3j8
```

## 🏁 Tổng kết
- `.bashrc` là file cấu hình cá nhân của **shell bash**, được thực thi mỗi lần mở một shell tương tác mới như vào `SSH`
- file `.bashrc` nằm trong thư mục **home** của người dùng.
