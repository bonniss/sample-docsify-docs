# Quản trị hệ thống

Hệ thống trên server được quản trị nhờ công cụ `pm2`. Chạy các lệnh sau trên terminal/bash/cmd/powershell.

## Khởi động CMS

```bash
# di chuyển đến thư mục backend
cd 'C:\zodiac\src\backend'

# khởi động ứng dụng
pm2 start ecosystem.config.js
```

?> Quản trị viên có thể cấu hình để đoạn script trên tự động chạy khi khởi động máy tính để hệ thống không bị gián đoạn

## Liệt kê các tiến trình

```bash
# Từ bất kỳ đường dẫn nào
pm2 list
```

Kết quả minh họa

```
┌────┬─────────────────────────┬──────────┬──────┬───────────┬──────────┬──────────┐
│ id │ name                    │ mode     │ ↺    │ status    │ cpu      │ memory   │
├────┼─────────────────────────┼──────────┼──────┼───────────┼──────────┼──────────┤
│ 0  │ zodiac-ranking-backend  │ fork     │ 0    │ online    │ 0%       │ 27.7mb   │
└────┴─────────────────────────┴──────────┴──────┴───────────┴──────────┴──────────┘
```

Hệ thống CMS là tiến trình có tên `zodiac-ranking-backend`. Mỗi tiến trình sẽ có id tương ứng. Id và tên này được sử dụng để định danh tiến trình khi quản trị.

## Bắt đầu một tiến trình

```bash
pm2 start <id>/<tên-ứng-dụng>
```

Áp dụng với kết quả minh họa

```bash
pm2 start 0
# hoặc
pm2 start zodiac-ranking-backend
```

## Khởi động lại một tiến trình

```bash
pm2 reload <id>/<tên-ứng-dụng>
```

Áp dụng với kết quả minh họa

```bash
pm2 reload 0
# hoặc
pm2 reload zodiac-ranking-backend
```

## Dừng một tiến trình

```bash
pm2 stop <id>/<tên-ứng-dụng>
```

Áp dụng với kết quả minh họa

```bash
pm2 stop 0
# hoặc
pm2 stop zodiac-ranking-backend
```

## Xóa một tiến trình

```bash
pm2 delete <id>/<tên-ứng-dụng>
```

Áp dụng với kết quả minh họa

```bash
pm2 delete 0
# hoặc
pm2 delete zodiac-ranking-backend
```
