# Tạo trang tài liệu

Việc thêm trang tài liệu chỉ đơn giản là thêm file markdown:

- `docsify` sẽ dùng đường dẫn tương đối của file để tạo đường dẫn truy cập sau dấu `#`.
- Tên file `README.md` là tên file mặc định đến một thư mục (như `index.html`).

```txt
.
└── docs
    ├── README.md
    ├── guide.md
    └── zh-cn
        ├── README.md
        └── guide.md
```

Đường dẫn tương ứng:

```txt
docs/README.md        => http://domain.com
docs/guide.md         => http://domain.com/#/guide
docs/zh-cn/README.md  => http://domain.com/#/zh-cn/
docs/zh-cn/guide.md   => http://domain.com/#/zh-cn/guide
```
