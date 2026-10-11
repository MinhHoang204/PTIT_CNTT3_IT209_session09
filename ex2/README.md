# REPORT - Session 09 - Exercise 2
## Khởi chạy Web Server Nginx với Port Mapping
## 1. Khởi chạy container Nginx
### Lệnh chạy
```bash
docker run -d -p 8080:80 --name my-web nginx:alpine
```

### Kết quả đầu ra
```bash
```

## 2. Kiểm tra container đang chạy
### Lệnh chạy
```bash
docker ps
```

### Kết quả đầu ra
```bash
[Paste kết quả của lệnh "docker ps" tại đây]
```

## 3. Kiểm tra phản hồi từ web server
### Lệnh chạy
```bash
curl http://localhost:8080
```

### Kết quả đầu ra
```html
[Paste mã HTML trả về, đảm bảo có dòng "Welcome to nginx!"]
```

## 4. Dọn dẹp container
### Lệnh chạy
```bash
docker stop my-web && docker rm my-web
```

### Kết quả đầu ra
```bash
[Paste kết quả của lệnh stop và rm tại đây]
```

## Kết luận
- [ ] Container `my-web` khởi chạy thành công ở chế độ nền.
- [ ] Port 8080 được ánh xạ đúng tới cổng 80 trong container.
- [ ] Lệnh `curl http://localhost:8080` trả về mã HTML có dòng chữ `Welcome to nginx!`.
- [ ] Container đã được dừng và xóa thành công.