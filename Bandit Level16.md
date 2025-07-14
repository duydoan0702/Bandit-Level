
# Bandit Level

## 🧩 Challenge: Level 16

### 📝 Description
Mật khẩu cho level tiếp theo được lấy lại bằng cách gửi mật khẩu của level hiện tại đến **port** có phạm vi từ 31000 đến 32000.
Đầu tiên hãy tìm port nào nghe trong các port này.Sau đó tìm xem cổng nào hổ trợ **SSL/TLS&** cổng nào không.Chỉ có một máy chủ gửi cho bạn password level tiếp theo, các máy chủ khác chỉ gửi lại mọi thứ mà bạn gửi.

> Link: https://overthewire.org/wargames/bandit/bandit17.html

---

## 📖 Helpful Reading Material

**1. Port**
- Là số hiệu đặc biệt để phân biệt các dịch vụ khác nhau trên cùng địa chỉ IP.
- Phân biệt các dịch vụ trên server để giao tiếp với client.

## Công cụ

## 🧠 Chiến lược giải
- tìm hiểu công cụ **OpenSSL** để kết nối tới server và gửi mật khẩu của level hiện tại.

---

## 🛠️ Cách giải

1. Sử dụng câu lệnh sau để kết nối tới server

```
openssl s_client -connect localhost:30001

```

2. Gửi mật khẩu của level hiện tại để lấy mật khẩu level tiếp theo
---

## 🏁 Password

```
kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx

```

## 📚 Tổng Kết

  - Câu lệnh `openssl s_client -connect host:port` là công cụ hữu ích để giao tiếp với dịch vụ sử dụng `SSL` để gửi dữ liệu.
