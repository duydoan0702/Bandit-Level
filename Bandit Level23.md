
# Bandit Level

## 🧩 Challenge: Level 22

## 📝 Description
Một chương trình đang chạy tự động theo các khoảng thời gian đều đặn từ cron, trình lập lịch tác vụ theo thời gian. Hãy xem cấu hình trong /etc/cron.d/ và xem lệnh nào đang được thực thi.

LƯU Ý: Việc xem các tập lệnh shell do người khác viết là một kỹ năng rất hữu ích. Tập lệnh ở cấp độ này được thiết kế để dễ đọc. Nếu bạn gặp khó khăn khi hiểu chức năng của nó, hãy thử chạy nó để xem thông tin gỡ lỗi được in ra.


> Link: https://overthewire.org/wargames/bandit/bandit23.html

---

## 🧠 Chiến lược giải
- Tìm hiểu các dòng lệnh shell để tìm được password level tiếp theo.
---


## 🛠️ Cách giải

1. Theo mô tả ta vào đường dẫn `/etc/cron.d/` và kiểm tra

```
cat cronjob_bandit23
```
-> Đọc file cronjob_bandit23

2.Theo mô tả của file ta vừa kiểm tra ở trên, ta tiếp tục:

```
cat /usr/bin/cronjob_bandit23.sh
```

3.Tìm hiểu các dòng lệnh shell ở trên và thực hiện:

```
echo "I am user bandit23" | md5sum | cut -d ' ' -f 1
```
-> sau đó ta nhận được chuỗi sau : `8ca319486bfbbc3663ea0fbe81326349`

4.Ta thưc hiện lệnh sau để lấy password

```
cat /tmp/8ca319486bfbbc3663ea0fbe81326349
```

---


## 🏁 Password

```
0Zf11ioIjMVN551jX3CmStKLYqjk54Ga
```
