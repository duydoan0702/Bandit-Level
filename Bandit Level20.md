
# Bandit Level

## 🧩 Challenge: Level 20

### 📝 Description
Có một tệp nhị phân setuid trong thư mục home thực hiện chức năng sau: nó tạo kết nối đến localhost trên cổng bạn chỉ định làm đối số dòng lệnh. Sau đó, nó đọc một dòng văn bản từ kết nối và so sánh với mật khẩu ở cấp độ trước đó (bandit20). Nếu mật khẩu đúng, nó sẽ truyền mật khẩu cho cấp độ tiếp theo (bandit21).

LƯU Ý: Hãy thử kết nối với daemon mạng của riêng bạn để xem nó có hoạt động như bạn nghĩ không.


> Link: https://overthewire.org/wargames/bandit/bandit21.html

---

## 🧠 Chiến lược giải
- Mở một `port` với chế độ `listener` sau đó dùng tệp thực thi `./suconnect` để kết nối và đọc dữ liệu.

---


## 🛠️ Cách giải

1. Kiểm tra các file, folder kể cà file ẩn

```
ls -la
```
- Ta thấy tệp `suconnect` là một chương trình thực thi.Theo mô tả, nó yêu cầu bạn kết nối đến một listener đang chờ nhận dữ liệu tại một cổng cụ thể.

2. Mở một `listener` đến một `port` cụ thể.
### Cách 1: Thực hiện với 2 Terminal
- Terminal A: Mở `port`
```
nc -l 1234
```
-> Mở port 1234 với chế độ `listener` đợi ` chương trình khác kết nối.

- Terminal B: chạy `./suconnect` để kết nối và đọc dữ liệu

```
./suconnect 1234
```
- Kết nối tới `port` 1234 nhận và đọc dữ liệu từ đó nếu đúng password sẽ trả lại nextlevel password.

### Cách 2: Thực hiện với 1 Terminal

```
echo "0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO" | nc -l 1234 &
```
-> `echo` gửi mật khẩu vào `netcat`, dùng `&` để chạy nền cho phép bạn thực hiện câu lệnh khác.

```
./suconnect 1234
```
-> Kết nối `port` 1234, đọc password nếu đúng sẽ nhận được nextlevel password.


---

## 🏁 Password

```
EeoULMCra2q0dSkYj561DX7s1CpBuOBt
```
