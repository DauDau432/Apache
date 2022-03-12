# Apache
## Trên ubuntu
### Cài đặt Apache
```
sudo apt install apache2 -y
```
### Quản lý Apache
kiểm tra trạng thái của Apache 
```
sudo systemctl status apache2
```
bật và khởi động dịch vụ Apache
```
sudo systemctl enable apache2
sudo systemctl start apache2
```
Để dừng Apache, dùng lệnh:
```
sudo systemctl stop apache2
```
Lệnh khởi động lại Apache:
```
sudo systemctl restart apache2
```
Tải lại dịch vụ Apache mỗi khi bạn thay đổi cấu hình:
```
sudo systemctl reload apache2
```

## Trên centos
### Cài đặt Apache
```
sudo yum install httpd -y
```
### Quản lý Apache
bật và khởi động dịch vụ Apache
```
systemctl enable httpd
systemctl start httpd
```
kiểm tra trạng thái của Apache 
 ```
systemctl status httpd
 ```
Để dừng Apache, dùng lệnh:
```
systemctl stop httpd
```
Lệnh khởi động lại Apache:
```
systemctl restart httpd
```
Tải lại dịch vụ Apache mỗi khi bạn thay đổi cấu hình:
```
systemctl reload httpd
```
Nếu các bạn sử dụng Firewalld để có thể truy cập được website các bạn sẽ cần mở port bằng các lệnh sau đây
```
firewall-cmd --permanent --zone=public --add-service=http
firewall-cmd --permanent --zone=public --add-service=https
firewall-cmd --reload
```
Hoặc các bạn copy đoạn lệnh dưới đây cho nhah 
```
sudo yum install httpd
sudo service httpd start
sudo service httpd status
sudo chkconfig httpd on
```
Tạo trang đầu tiên
```
vi /var/www/html/index.html
```
Viết đoạn code bố cục đầu tiên cho trang 
```
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>First Website</title>
</head>
<body>
	<h1>First Website</h1>
</body>
</html>
```





