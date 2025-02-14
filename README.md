# Tài liệu mẫu sử dụng Docsify

## Trước khi bắt đầu

> Node.js >= v10

Cài đặt docsify với scope global:

```sh
npm i docsify-cli -g
```

## Bắt đầu

Từ thư mục gốc, chạy:

```bash
npm start
```

hoặc chạy thẳng:

```sh
docsify serve ./docs
```

hoặc từ bên trong thư mục `docs`:

```sh
docsify serve .
```

Trang tài liệu được triển khai ở địa chỉ: [http://localhost:3000](http://localhost:3000)

## Hướng dẫn biên soạn

Nội dung tài liệu nằm trong thư mục `docs`.

- Nội dung trang chủ nằm tại: `docs/readme.md`.
- Nội dung thanh điều hướng nằm tại: `docs/_sidebar.md`.
- Nội dung trang sẽ được render trên trang html `docs/index.html`.
- Các file tài nguyên: hình ảnh, video, MS Word, PDF... lưu tại `docs/assets`.

Các file còn lại là các trang nội dung viết bằng Markdown.

## Deploy

Chỉ đơn giản là bê tất cả nội dung của thư mục `docs` và đưa lên server làm web tĩnh.

## Tra cứu

[Tài liệu chính thức của Docsify](https://docsify.js.org/#/)
