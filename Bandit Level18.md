
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
ssh abndit18@bandit.labs.overthewire.org -p 2220 "cat /home/bandit18/readme"
```



---

## 🏁 Password

```

```
