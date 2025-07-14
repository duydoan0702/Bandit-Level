
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

## 🔧 Công cụ
**1. Nmap**
- Dùng để quét mạng, kiểm tra cổng(port), dịch vụ và hệ điều hành mục tiêu.
- Xác định lỗ hổng bảo mật, kiểm tra tường lửa, giám sát mạng.
- Câu lệnh:

📌 1. Quét 1 địa chỉ IP với cổng mặc định:

```
nmap 192.168.1.1
```
📌 2. Quét một dải cổng đang hoạt động:

```
nmap -p 31000-32000 localhost
```
📌 3. Quét tất cả **65535** cổng

```
nmap -p- localhost
```
📌 4. Hiển thị tên dịch vụ đang chạy

```
nmap -sV localhost
```
📌 5. Kiểm tra hệ điều hành đang chạy

 ```
sudo nmap -O localhost

````
## 🧠 Chiến lược giải
- Kiểm tra các port đang hoạt đông, sau đó tìm port có dịch vị SSL hoặc TLS để gửi dữ liệu mật khẩu khẩu của level hiện tại.

---

## 🛠️ Cách giải

1. Sử dụng công cụ `Nmap` để kiểm tra các `port` đang hoạt động

```
nmap -p 31000-32000 localhost

```

2. Kiểm tra các dịch vụ **SSL/TLS** trên các cổng để gửi current password.
  
```
nmap -sV -p 31000-32000 localhost 
```
3. kết nối tới các cổng có dịch vụ **SSL** để gửi mật khẩu.

```
openssl s_client -connect localhost:31790 -quite
```
- `-quiet` : sẽ tắt mọi dòng in ra thêm từ OpenSSL, chỉ giữ lại dữ liệu bạn nhập vào và dữ liệu server trả lại.
- nhập mật khẩu sau để nhập `private key`:

```
kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx

```

```

-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnPw9nC
YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlpmS8A
vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sOmama
+TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRRhORT
8c8hAuRBb2G82so8vUHk/fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx
SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEAypHd
HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/b0iE7KaszX+Exdvt
SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5SiWg0A
R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V5HDi
Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/lemmEY5eTDAFMLy9FL2m9oQWCg
R8VdwSk8r9FGLS+9aKcV5PI/WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu
L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOmL8Ni
blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/ZJQ7YfzOKU4ZxEnabvXnvWkU
YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM
77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9Cq0b
dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3
vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
-----END RSA PRIVATE KEY-----

```
4. lưu private key vào file tạm thời

```
echo "<private key>" > /tmp/bandit17.key
```
-> SSH cần file chứa khóa riêng để xác thực

5. Đặt quyền truy cập an toàn cho file private key

```
chmod 600 /tmp/bandit17.key
```
-> Trong SSH file có quyền rộng hơn `644` sẽ bị lỗi

6. Dùng SSH key để đăng nhập vào level 17

```
ssh -i /tmp/bandit17.key bandit17@localhost -p 2220
```


---

## 🏁 Password

```

```

## 📚 Tổng Kết
- SSH key : Dùng để xác thực không cần mật khẩu
- Ghi key : có thể dùng `cat >`, `nano`, hoặc `vim` tránh dùng `echo`
