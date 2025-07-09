
# Bandit Level

## 🧩 Challenge: Level 12

### 📝 Description
mật khẩu được lưu trong data.txt, là một `hex dump` của một tệp đã được giải nén nhiều lần, hãy xử lí nhiều các lớp giải nén đố để lấy được password.


> Link: https://overthewire.org/wargames/bandit/bandit13.html

---

## 🧠 Chiến lược giải
- Đối với cấp độ này, có thể hữu ích khi tạo một thư mục trong `/tmp` mà bạn có thể làm việc. Sử dụng `mkdir` với tên thư mục khó đoán. Hoặc tốt hơn, sử dụng lệnh `mktemp -d`. Sau đó sao chép tệp dữ liệu bằng cp và đổi tên bằng mv

---

## 🛠️ Cách giải

1. tạo thư mục làm việc tạm thời và sao chép dữ liệu

```
mkdir /tmp/banditlevel12
cd /tmp/banditlevel12
cp ~/data.txt .
```
  ->   câu lệnh `mkdir` để tạo thư mục mới `banditlevel12` trong thư mục gốc `tmp`

  ->   câu lệnh `cd` để chuyển tới thư mục `banditlevel12`

  ->   câu lệnh `cp` để sao chép dữ liệu từ file `data.txt` trong thư mục chính (`~`) sang thư mục hiện tại (`.`)
2. chuyển hex dump về file nhị phân

```
xxd -r data.txt > newdata.txt

```
-> `xxd -r` (`-r` : reverse) : chuyển file hex về file nhị phân gốc
-> kết quả lưu vào file `newdata.txt`

3. Giải nén `Gzip` đầu tiên

```
file newdata.txt
mv newdata.txt newdata.tar.gz
```
![image](https://github.com/user-attachments/assets/279f459b-488d-4889-b1d7-892ae019cd6e)

-> câu lệnh `file` để kiểm tra kiểu file, ta thấy `gzip compressed data` nghĩa là file đang ở định dạng giải nén `gzip` 
-> ta chuyển về đúng định dang bằng câu lệnh `mv newdata.txt newdata.tar.gz`
-> dùng `gunzip` để giải nén

## 🏁 Password
```

```

## 📚 Tổng Kết
