# Bandit Level

## 🧩 Challenge: Level 14

### 📝 Description
Mật khẩu của level tiếp theo có được lấy lại bằng cách gửi mật khẩu của cấp độ hiện tại lên port `30000` của máy chủ

> Link: https://overthewire.org/wargames/bandit/bandit15.html

---

## 📖 Helpful Reading Material
**1. Internet hoạt động như thế nào ?**
- Internet hoạt động như một sợi dây kết nối các máy tính, các máy chủ sẽ kết nối trực tiếp tới **Internet** . Các client kết nối thông qua **ISP ( Internet Service Provider)** .Thông tin trên Internet được chia thành các gói nhỏ **(packet)** được định tuyến truyên Internet bằng địa chỉ **IP** để đảm bảo đến đúng đích.
  
  <img width="400" height="300" alt="image" src="https://github.com/user-attachments/assets/92a04303-93a0-468d-a7be-9f1e5f4a5f09" />

  

## 🧠 Chiến lược giải
- tìm câu lệnh để nối tới server và gửi mật khẩu cũ cho server để lấy mật khẩu mới.

---

## 🛠️ Cách giải

1. Kết nối với server thông qua **telnet**
```
telnet localhost 30000
```
-> telnet chỉ nhận đối số `host` và `port`

 2. nhập mật khẩu để gửi cho server

```
MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS
```
---

## 🏁 Password

```
8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo

```

## 📚 Tổng Kết

  - Muốn 1 client kết nối tới server cần **IPAddress** và **Port**
