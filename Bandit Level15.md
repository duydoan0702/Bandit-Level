# Bandit Level

## 🧩 Challenge: Level 15

### 📝 Description
Mật khẩu của cấp độ tiếp theo có thể được lấy lại bằng cách gửi mật khẩu của cấp độ hiện tại tới port `300001` trên `localhost` bằng mã hóa `SSL/TLS`

> Link: https://overthewire.org/wargames/bandit/bandit16.html

---

## 📖 Helpful Reading Material

**1. Kiểm tra bảo mật TLS**
- Dùng `Hardennize` để kiểm tra online
- Dùng `testssl.sh` để kiểm tra offline

**2.SSL ( Secure Socket Layer ) và TLS ( Transport Layer Security)**
- Là giao thức bảo mật của tầng **Transport Layer**, Giúp:
      + Mã hóa dữ liệu truyền đi trên mạng
      + Xác thực danh tính máy chủ/khách.
      + Đảm bỏa tính toàn vẹn dữ liệu.
- **TLS** là phiên bản kế thừa bảo mật hơn **SSL**, hiện nay **TLS 1.2** và **TLS 1.3** được sử dụng phổ biến.

  

## 🧠 Chiến lược giải
- tìm hiểu công cụ **OpenSSL** để kết nối tới server và gửi mật khẩu của level hiện tại.

---

## 🛠️ Cách giải

1. Sử dụng câu lệnh sau để kết nối tới server

```
opensll s_client -connect localhost:30001

```

2. Gửi mật khẩu của level hiện tại để lấy mật khẩu level tiếp theo
---

## 🏁 Password

```
kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx

```

## 📚 Tổng Kết

  - Câu lệnh `openssl s_client -connect host:port` là công cụ hữu ích để giao tiếp với dịch vụ sử dụng `SSL` để gửi dữ liệu.
