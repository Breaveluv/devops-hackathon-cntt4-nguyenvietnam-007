#DevOps Hackathon Đề 007 : Đặt vé xe Bus


##1: Thông tin sinh viên
|Họ và tên|MSSV|Lớp|Tài khoản Linux|Github| Cổng nginx|
|---|---|---|---|---|---|
|Nguyễn Văn A|123456|KTPM01|nguyenvana|nguyenvana|8080|
|Nguyễn Việt Nam|123457|KTPM01|nguyenvietnam|nguyenvietnam|8081|
|Nguyễn Văn B|123458|KTPM01|nguyenvanb|nguyenvanb|8082|

## 2: Môi trường phát triển 
(hệ điều hành, phiên bản Nginx, Git, nơi chạy)
    VPS: Ubuntu 22.04, Nginx 1.18, Git 2.34, chạy trên VPS
## 3 : Cấu trúc thư mục 
devops-hackathon-007-nguyenvietnam/
├── src/
    ├── index.html
├──nginx/
    ├──nguyenvietnam-cntt4.conf
├── screenshots/
├──.gitignore
├──README.md

## 4: Cấu hình Nginx
|Tham số trong templet|Giá trị|Giải thích|
|---|---|---|
|server_name|nguyenvietnam|Tên miền ảo|
|listen|8081|Cổng lắng nghe|
## 5: Tường lửa
(các rule đã thêm+ kết quả `sudo ufw status`)
|Rule|Kết quả|
|---|---|
|sudo ufw allow 8081/tcp|Rule added|

## 6: Các bước triển khai 
(các lệnh đã chạy, theo đúng thứ tự)
1. Cài đặt Nginx: `sudo apt install nginx`
2. Cấu hình Nginx: `sudo nano /etc/nginx/sites-available/nguyenvietnam-cntt4.conf`
3. Kích hoạt cấu hình: `sudo ln -s /etc/nginx/sites-available/nguyenvietnam-cntt4.conf /etc/nginx/sites-enabled/`
4. Kiểm tra cấu hình: `sudo nginx -t`
5. Khởi động lại Nginx: `sudo systemctl restart nginx`

## 7: Kiểm tra & minh chứng

## 8:Quy trình cập nhật website

## 9 : Các vấn đề gặp phải nếu có