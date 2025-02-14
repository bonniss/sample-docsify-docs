# Hình ảnh & file cho tải xuống

Quy ước hình ảnh & file cho tải xuống nằm trong thư mục `_media`.

## Hình ảnh

Cú pháp của markdown cho chèn hình ảnh. Lưu ý dấu `!` ở đầu so với đường dẫn thông thường trong markdown.

~~~md
```md
<!-- Đường dẫn tuyệt đối -->
![alt text](https://placehold.co/600x400)

<!-- Đường dẫn tương đối đến file trong _media -->
![alt text](../_media/logo.png)
```
~~~

## File cho tải xuống

Tải file xuống chỉ đơn giản là tạo đường dẫn đến file. Lưu ý điểm khác so với cú pháp chèn ảnh là đường dẫn không có dấu `!` ở đầu.

~~~md
```md
<!-- Đường dẫn tuyệt đối -->
[My portfolio](https://topcv.fake/portfolio.pdf)

<!-- Đường dẫn tương đối đến file trong _media -->
[My portfolio](../_media/portfolio.pdf)
```
~~~
