
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
- Câu lệnh:
- 
📌 1. Quét 1 địa chỉ IP với cổng mặc định:
```
nmap 192.168.1.1
```
📌 2. Quét một dải cổng đang hoạt động:

```
nmap -p 31000-32000 localhost
```
📌 3. Kiểm tra các dịch vụ **SSL/TLS** trên 
```
nmap -p- localhost
```
📌 4. 



## 🔧 Công cụ
**1. Nmap**
- Dùng để quét mạng, kiểm tra cổng(port), dịch vụ và hệ điều hành mục tiêu.
- Xác định lỗ hổng bảo mật, kiểm tra tường lửa, giám sát mạng.

## 🧠 Chiến lược giải
- 

---

## 🛠️ Cách giải

1. Sử dụng công cụ `Nmap` để kiểm tra các `port` đang hoạt động

```
nmap -A -p 31000-32000 localhost

```
- `-A` : Bất chệ độ quét nâng cao( phát hiện hệ điều hành, dịch vụ, sript scanning, traceroute)

2. 
---

## 🏁 Password

```
kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx

```

## 📚 Tổng Kết

  - Câu lệnh `openssl s_client -connect host:port` là công cụ hữu ích để giao tiếp với dịch vụ sử dụng `SSL` để gửi dữ liệu.
