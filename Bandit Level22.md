
# Bandit Level

## 🧩 Challenge: Level 21

## 📝 Description
Một chương trình đang chạy tự động theo các khoảng thời gian đều đặn từ cron, trình lập lịch tác vụ theo thời gian. Hãy xem cấu hình trong /etc/cron.d/ và xem lệnh nào đang được thực thi.

> Link: https://overthewire.org/wargames/bandit/bandit22.html

---

## 🧠 Chiến lược giải
- Tìm hiểu về `cron` 

## 🔧 Công cụ
1. **Cron**
- Cron là một daemon (dịch vụ chạy nền), tự động thực hiện các tác vụ theo lịch trình do người dùng chỉ định.
- Các tác vụ này được lưu trong crontab – viết tắt của “cron table”.

---


## 🛠️ Cách giải

1. Theo gợi ý đề ta vào đường dẫn `etc/cron.d/` để kiểm tra các `cronjobs`

```
cat cronjob_bandit22
```
-> kiểm tra nội dung file

<img width="651" height="147" alt="image" src="https://github.com/user-attachments/assets/e0e6486c-f7ce-4999-94ee-abf8739350f5" />

- `chmod644` điều này có nghĩa là bất kì ai cũng có thể đọc nội dung của file, điều này là lổ hổng bảo mật.

2. Đọc nội dung file tạm và lấy password

```
cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
```


---

## 🏁 Password

```
tRae0UfB9v0UzbCdn9cY0gQnds9GF58Q
```
