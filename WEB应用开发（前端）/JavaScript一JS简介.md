# 第1关：JavaScript 语言介绍、注释及基本输出方式

## 采用相关知识板块介绍的任意一种方法，实现输出“ Hello,JavaScript! ”。

```javascript
document.write("Hello,JavaScript!");
```


# 第2关：JavaScript 与 HTML

## 将下面的 JavaScript 代码嵌入到 HTML 代码中；必须使用内置代码的方式

```html
<head>
        <script>
            console.log("如何在HTML代码中嵌入JavaScript代码");
            </script>
	</head>
	<body>
	</body>
```


# 第3关：JavaScript变量

## 定义一个局部变量a，并赋值使其覆盖已有的全局变量a；定义一个全局变量b并初始化之；上面两步必须使得函数variableTest返回100+10*c，c为输入；

```javascript
var a;
var b = 100;
a = 10;
```