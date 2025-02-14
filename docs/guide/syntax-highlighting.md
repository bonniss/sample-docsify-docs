# Làm nổi cú pháp cho code

Trong Markdown, code block có thể được khai báo bằng ` ``` ` hoặc `~~~`, theo đuôi là tên ngôn ngữ trong block.

~~~md
```java
// java code
```
~~~

Docsify sử dụng [Prism](https://prismjs.com/#supported-languages) để làm nổi cú pháp cho code block.

Prism hỗ trợ mặc định các ngôn ngữ sau:

- Markup - `markup`, `html`, `xml`, `svg`, `mathml`, `ssml`, `atom`, `rss`
- CSS - `css`
- C-like - `clike`
- JavaScript - `javascript`, `js`

Tài liệu đã cấu hình thêm các ngôn ngữ sau:

- C#
- ASP.NET
- T4 templating engine
- Java
- Javadoc-like
- JSON
- Bash
- Mermaid
- Javascript
- Typescript
- TSX
- SQL
- Docker

Đó là lý do bạn thấy màu sắc của code block dưới đây cho ASP.NET và C#:

```aspnet
<!-- directives -->
<% @Page Language="C#" %>

<!-- code section -->
<script runat="server">

   private void convertoupper(object sender, EventArgs e)
   {
      string str = mytext.Value;
      changed_text.InnerHtml = str.ToUpper();
   }
</script>

<!-- Layout -->
<html>
   <head> 
      <title> Change to Upper Case </title> 
   </head>
   
   <body>
      <h3> Conversion to Upper Case </h3>
      
      <form runat="server">
         <input runat="server" id="mytext" type="text" />
         <input runat="server" id="button1" type="submit" value="Enter..." OnServerClick="convertoupper"/>
         
         <hr />
         <h3> Results: </h3>
         <span runat="server" id="changed_text" />
      </form>
      
   </body>
   
</html>
```

```csharp
public static void Main()
  {
    // Declaration statement.
    int counter;

    // Assignment statement.
    counter = 1;

    // Error! This is an expression, not an expression statement.
    // counter + 1;

    // Declaration statements with initializers are functionally
    // equivalent to  declaration statement followed by assignment statement:
    int[] radii = [15, 32, 108, 74, 9]; // Declare and initialize an array.
    const double pi = 3.14159; // Declare and initialize  constant.

    // foreach statement block that contains multiple statements.
    foreach (int radius in radii)
    {
      // Declaration statement with initializer.
      double circumference = pi * (2 * radius);

      // Expression statement (method invocation). A single-line
      // statement can span multiple text lines because line breaks
      // are treated as white space, which is ignored by the compiler.
      System.Console.WriteLine("Radius of circle #{0} is {1}. Circumference = {2:N2}",
                              counter, radius, circumference);

      // Expression statement (postfix increment).
      counter++;
    } // End of foreach statement block
  } // End of Main method body.
} // End of SimpleStatements class.
/*
   Output:
    Radius of circle #1 = 15. Circumference = 94.25
    Radius of circle #2 = 32. Circumference = 201.06
    Radius of circle #3 = 108. Circumference = 678.58
    Radius of circle #4 = 74. Circumference = 464.96
    Radius of circle #5 = 9. Circumference = 56.55
*/
```

...nhưng block PHP thì vô sắc:

```php
<?php
$x = 5;
$y = 10;

function myTest() {
  $GLOBALS['y'] = $GLOBALS['x'] + $GLOBALS['y'];
}

myTest();
echo $y;
?>
```

Bởi `php` chưa được cấu hình với Prism. Để cài đặt chỉ cần đặt đúng script cho ngôn ngữ đó ở cuối `<body>`:

```html
<script src="//cdn.jsdelivr.net/npm/prismjs@1/components/prism-php.min.js"></script>
```

Xem thêm [tại đây](https://github.com/docsifyjs/docsify/blob/develop/docs/language-highlight.md).
