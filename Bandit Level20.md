
# Bandit Level

## 🧩 Challenge: Level 19

### 📝 Description
Để có được password cho level tiếp theo, bạn nên sử dụng tệp nhị phân setuid trong thư mục home. Thực thi tệp nhị phân này mà không có đối số để tìm hiểu cách sử dụng. Mật khẩu cho cấp độ này có thể được tìm thấy ở vị trí thông thường (/etc/bandit_pass), sau khi bạn sử dụng tệp nhị phân setuid.

> Link: https://overthewire.org/wargames/bandit/bandit20.html

---

## 🧠 Chiến lược giải
- Tìm hiểu về **setuid**

## 🔧 Công cụ
1. **setuid (Set User ID)**
- là một permision bit đặc biệt trong hệ thống **Unix/Linux**. Khi được bật trên một tệp thực thi (executable file), nó cho phép người dùng chạy với quyền sở hữu file thay vì người đang thực thi nó.
- **Mục đích**: cho phép người dùng chạy với quyền hạn cao hơn thường là `root`.

---


## 🛠️ Cách giải

1. Kiểm tra thư mục `home`

```
ls -la
```
- kiểm tra các file, thực mục, kể cả các file ẩn

```
-rwsr-x--- 1 bandit20 bandit19 14884 Apr 10 14:23 bandit20-do
```
- ta thấy có quyền `rws` => đã bật `setuid`. khi chạy file này bạn sẽ có quyền của bandit20

2.đọc file `bandit20`

```
./bandit20-do cat /etc/bandit_pass/bandit20
```
- Vì chương trình bandit20-do đã bật setuid, nó sẽ thực thi lệnh cat dưới quyền bandit20, cho bạn đọc được password level tiếp theo.


---

## 🏁 Password

```
0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO
```
