
# Bandit Level

## 🧩 Challenge: Level 23

## 📝 Description
Một chương trình đang chạy tự động theo các khoảng thời gian đều đặn từ cron, trình lập lịch tác vụ theo thời gian. Hãy xem cấu hình trong /etc/cron.d/ và xem lệnh nào đang được thực thi.

LƯU Ý: Cấp độ này yêu cầu bạn phải tạo tập lệnh shell đầu tiên của riêng mình. Đây là một bước rất lớn và bạn nên tự hào khi vượt qua cấp độ này!

LƯU Ý 2: Lưu ý rằng tập lệnh shell của bạn sẽ bị xóa sau khi được thực thi, vì vậy bạn có thể muốn giữ một bản sao…


> Link: https://overthewire.org/wargames/bandit/bandit24.html

---

## 🧠 Chiến lược giải
- 
---


## 🛠️ Cách giải
1. Theo mô tả đề ta vào `/etc/cron.d/` để kiểm tra

```
cat cronjob_bandit24
```
Sau đó:
```
cat /usr/bin/cronjob_bandit24.sh
```
- sau khi đọc tệp shell ta nhận được đoạn mã ngôn ngữ `bash` như sau:
<img width="560" height="288" alt="image" src="https://github.com/user-attachments/assets/a209b67b-1a6a-4d65-b23a-1c2aa2881c36" />


---


## 🏁 Password

```
0Zf11ioIjMVN551jX3CmStKLYqjk54Ga
```
