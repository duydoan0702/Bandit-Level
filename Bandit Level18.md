
# Bandit Level

## 🧩 Challenge: Level 18

### 📝 Description
Mật khẩu cho cấp độ tiếp theo được lưu trong tệp readme trong thư mục home. Thật không may, ai đó đã sửa đổi .bashrc để đăng xuất bạn khi bạn đăng nhập bằng SSH.

> Link: https://overthewire.org/wargames/bandit/bandit19.html

---

## 🧠 Chiến lược giải
- tìm công cụ `diff` để tìm dòng lệnh khác nhau giữa 2 file, thử các dòng lệnh khác nhau đó để tìm password
---

## 🛠️ Cách giải

1. Dùng `ls` để kiểm tra xem các file trong thử mục `home`

2. Dùng `diff` để tìm câu lệnh khác nhau

```
diff passwords.new passwords.old
```
-> thử 2 passowrd khác nhau để tìm ra passowrd


---

## 🏁 Password

```
x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO
```
