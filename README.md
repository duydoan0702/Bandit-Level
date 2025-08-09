# 🔧Các công cụ

## 1. Netcat (nc)
- Chức năng chính: Đọc/ghi dữ liệu qua kết nối TCP hoặc UDP
- thường dùng để:
  
|  **Chức năng**                    |  **Máy 1 (Người nhận / Lắng nghe)**              |  **Máy 2 (Người gửi / Kết nối)**              |
|------------------------------------|---------------------------------------------------|------------------------------------------------|
|  **Kiểm tra port**                |                                                   | `nc -zv 192.168.1.1 80 443`                     |
|  **Gửi & nhận dữ liệu**          | `nc -l -p 1234`                                    | `echo "hello" \| nc [IP máy 1] 1234`           |
|  **Chuyển file giữa 2 máy**      | `nc -l -p 1234 > file.txt`                         | `nc [IP máy nhận] 1234 < file.txt`             |
|  **Kết nối giữa 2 máy (socket)** | `nc -l -p 1234`                                    | `nc [IP máy 1] 1234`                           |
|  **Chat giữa 2 máy**             | `nc -l -p 1234`                                    | `nc [IP máy 1] 1234`                           |

## 2.Shell
- Là một chương trình khởi chạy ngay sau khi bạn đăng nhập, thường là `/bin/bash/`, `/bin/sh`, `zsh` cho phép bạn gõ lệnh tự do
- Ở level 26 một chương trình tên `/usr/bin/showtext` làm shell mặc định, mỗi khi đăng nhập hệ thống sẽ **không mở dòng lệnh** mà chạy **showtext** ( `showtext` chỉ đơn giản là một script hiển thị một số nội dung mà tác giả muốn hạn chế người dùng truy cập shell thật rồi thoát )
