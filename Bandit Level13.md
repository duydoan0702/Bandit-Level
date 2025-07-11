
# Bandit Level

## 🧩 Challenge: Level 13

### 📝 Description

Mật khẩu cho cấp độ tiếp theo được lưu trữ trong /etc/bandit_pass/bandit14 và chỉ người dùng bandit14 mới có thể đọc được. Ở cấp độ này, bạn không nhận được mật khẩu tiếp theo, nhưng bạn sẽ nhận được khóa SSH private có thể được sử dụng để đăng nhập vào cấp độ tiếp theo. Lưu ý: localhost là tên máy chủ tham chiếu đến máy bạn đang làm việc.


> Link: https://overthewire.org/wargames/bandit/bandit14 .html

---

## 🧠 Chiến lược giải
- tìm hiểu về **SSH/OpenSSH/Keys** qua linh sau:
  
> Link: https://help.ubuntu.com/community/SSH/OpenSSH/Keys

---

## 🛠️ Cách giải

1.  kết nối tới bandit14 bằng `sshkey` 
   
```
ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220
```
| Pulic/Private Key | Cặp khóa này dùng để xác thực: **Public key trên server, Private key trên client**|
|:---------------:|:-------------------------------------------------------------------------:|

-> `-i` : sử dụng file private để xác thực

2. truy cập vào đường dẫn sau `/etc/bandit_pass` để lấy password

```
cat bandit14

```


---

## 🏁 Password

```
MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS

```

