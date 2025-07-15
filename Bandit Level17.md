
# Bandit Level

## 🧩 Challenge: Level 17

### 📝 Description
Có 2 tệp trong thư mục home: passwords.old và passwords.new. Mật khẩu cho cấp độ tiếp theo nằm trong passwords.new và là dòng duy nhất đã được thay đổi giữa passwords.old và passwords.new.

> Link: https://overthewire.org/wargames/bandit/bandit18.html

---

## 🔧 Công cụ
**1. diff**
- **diff (difference)** so sánh nội dung dòng theo dòng giữa hai file và hiển thị sự khác biệt, thường được dùng trong:

  + So sánh file cấu hình

  + Kiểm tra thay đổi mã nguồn

  + Debug file đầu vào/đầu ra

  + Làm việc với patch (.patch)
- câu lệnh:

```
diff file1 file2
```
## 🧠 Chiến lược giải
- tìm công cụ `diff` để tìm dòng lệnh khác nhau giữa 2 file, thử các dòng lệnh khác nhau đó để tìm password.
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

