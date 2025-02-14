# Điều chỉnh sidebar

## Chỉnh sửa nội dung

Nội dung file `_sidebar.md` là các `ul` trong markdown, lồng nhau nhiều cấp.

- Nếu `li` là văn bản thường, tạo nhóm link.
- Nếu `li` là link, tạo link.

```md
* Level 1 group
  * [Level 2 link](/level-2.md)
    * Level 3 group
      * [Level 4 link](/level-4.md)
    * [Level 3 link](/level-3.md)
```

## Tùy biến `title`

> `title` là tiêu đề hiện trên tab của browser.

Mặc định một trang sẽ có `title` là tên link trên sidebar.

```md
<!-- _sidebar.md -->
* [Level 3 link](/level-3.md)
```

Khi ở trang `/level-3.md` thì `title` trang sẽ là `Level 3 link`. Thay đổi `title` như sau:

```md
<!-- _sidebar.md -->
* [Level 3 link](/level-3.md "Awesome title")
```
