# REPORT - Session 09 - Exercise 4
## Lưu trữ dữ liệu đơn giản với Docker Volume
## 1. Tạo volume mới
### Lệnh chạy
```bash
docker volume create easy-volume
```

### Kết quả đầu ra
```bash
easy-volume
```

## 2. Kiểm tra danh sách volume
### Lệnh chạy
```bash
docker volume ls
```

### Kết quả đầu ra
```bash
DRIVER    VOLUME NAME
local     easy-volume
```

## 3. Ghi dữ liệu vào volume (Container Alpine thứ nhất)
### Lệnh chạy
```bash
docker run --rm -v easy-volume:/data alpine sh -c "echo 'Luu tru du lieu Docker' > /data/test.txt"
```

### Kết quả đầu ra
```bash
(không có output - lệnh chạy thành công)
``

## 4. Đọc lại dữ liệu từ volume (Container Alpine thứ hai)
### Lệnh chạy
```bash
docker run --rm -v easy-volume:/data alpine cat /data/test.txt
```

### Kết quả đầu ra
```
Luu tru du lieu Docker
```

## Kết luận
- [ ] Volume `easy-volume` được tạo thành công.
- [ ] Container thứ nhất ghi dữ liệu vào volume thành công.
- [ ] Container thứ hai đọc lại được đúng chuỗi `Luu tru du lieu Docker`.
- [ ] Dữ liệu trong volume **không bị mất** khi container dừng và bị xóa (nhờ `--rm`).