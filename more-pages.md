## Tạo trang tài liệu mới

Để có thể thêm trang mới cho tài liệu của bạn, hãy tạo thêm một file markdown mới trong thư mục `./docs`. Ví dụ:

```text
.
└── docs
    ├── README.md
    ├── guide.md
    └── zh-cn
        ├── README.md
        └── guide.md
```

Nó sẽ tương ứng với các đường dẫn sau

```text
docs/README.md        => http://domain.com
docs/guide.md         => http://domain.com/#/guide
docs/zh-cn/README.md  => http://domain.com/#/zh-cn/
docs/zh-cn/guide.md   => http://domain.com/#/zh-cn/guide
```

##Thanh bên

Để có một thanh bên, bạn phải tạo tệp `_sidebar.md`, xem chi tiết tại đây.

Sau đó bạn phải đặt thuộc tính `loadSidebar` bằng **true**, chi tiết tại đây.

```html
<!-- index.html -->

<script>
  window.$docsify = {
    loadSidebar: true
  }
</script>
<script src="//cdn.jsdelivr.net/npm/docsify/lib/docsify.min.js"></script>
```

Ví dụ với nội dung tệp `_sidebar.md` như sau:

```markdown
<!-- docs/_sidebar.md -->

* [Home](/)
* [Guide](guide.md)
```

