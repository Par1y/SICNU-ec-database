# 第1关：初识CSS：丰富多彩的网页样式
## 修改h1标题的text-align为居中显示，字体大小为40px；p段落的颜色为灰色:grey,字体大小为18px。
```css
h1 {
    text-align: center;
    font-size: 40px;
}
p {
    color: grey;
    font-size: 18px;
}
```


# 第2关：CSS样式引入方式

## 选择index.html文件，完成：引入外部样式表style.css，引入的路径为step2/CSS/style.css；(注意路径中CSS是大写)，设置h1元素内联样式的字体颜色(color)为cornflowerblue，修改samll元素内联样式：设置字体大小(font-size)为10px; 颜色(color)为lightslategray。选择style.css文件，完成：设置p元素的font-weight为粗体(bold)。

```html
<link rel="stylesheet" href="">
<h1 >O Captain! My Captain!</h1>
 <p><small >&copy; Walt Whitman</small></p>
```

```css
font-weight: bold
```