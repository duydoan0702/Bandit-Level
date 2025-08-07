# 🔧Các công cụ

## 1. Netcat (nc)
- Chức năng chính: Đọc/ghi dữ liệu qua kết nối TCP hoặc UDP
- thường dùng để:
|  **Chức năng**                    |  **Máy 1 (Người nhận / Lắng nghe)**              |  **Máy 2 (Người gửi / Kết nối)**              |
|------------------------------------|---------------------------------------------------|------------------------------------------------|
|  **Kiểm tra port**                | –                                                 | `nc -zv 192.168.1.1 80 443`                    |
|  **Gửi & nhận dữ liệu**          | `nc -l -p 1234`                                    | `echo "hello" \| nc [IP máy 1] 1234`           |
|  **Chuyển file giữa 2 máy**      | `nc -l -p 1234 > file.txt`                         | `nc [IP máy nhận] 1234 < file.txt`             |
|  **Kết nối giữa 2 máy (socket)** | `nc -l -p 1234`                                    | `nc [IP máy 1] 1234`                           |
|  **Chat giữa 2 máy**             | `nc -l -p 1234`                                    | `nc [IP máy 1] 1234`                           |
