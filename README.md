# 🔧Các công cụ

## 1. Netcat (nc)
- Chức năng chính: Đọc/ghi dữ liệu qua kết nối TCP hoặc UDP
- thường dùng để:
    - Kiểm tra port `nc -zv 192.168.1.1 80 443`
    - Gửi và nhận dữ liệu mạng: người nhận `nc -l -p 1234`, người gửi `echo "hello" | nc [IP máy 1] 1234`
    - Chuyển file giữa 2 máy: máy nhận `nc -l -p 1234 > file.txt`, máy gửi `nc [IP máy nhận] 1234 < file.txt`
    - Kết nối giữa 2 máy ( giống như socket ): máy nghe `nc -l -p 1234` , máy kết nối `nc [IP máy 1] 1234`
    - Chat giữa 2 máy: máy nghe `nc -l -p 1234`, máy kết nối `nc [IP máy 1] 1234`
    - 
