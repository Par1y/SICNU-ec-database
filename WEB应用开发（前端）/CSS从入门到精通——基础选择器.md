# 第1关：CSS 元素选择器

## 使用元素选择器修改页面样式，要求如下：设定html元素的background-color为#F0F0F0；设定header元素的padding为40px，background-color为白色；添加footer元素的font-size为0.6em，字体颜色为灰色(grey)。

```css
html {
      background-color: #F0F0F0;
    }

    header {
      padding: 40px;
      background-color: white;
    }

    footer {
      margin-top: 20px;
      font-size: 0.6em;
      color: grey;
    }
```


# 第2关：CSS类选择器

## 使用类选择器修改页面样式，具体要求入下：给第43行的div元素添加名字为newsSection的类；在第27行添加newsSection类的样式：外边距为20（margin-top: 20px;）内边距为20（padding: 20px;）和背景颜色白色（background-color: white;）。

```css
.newsSection {
      margin-top: 20px;
      padding: 20px;
      background-color: white;
    }
```
```html
<div class="newsSection">
```


# 第3关：CSS id选择器

## 为header元素添加名为menu的id；使用id选择器，设置精选(#chosen)标题为红色(red)，时事( #news)标题为蓝色(blue)，财政(#finance)标题为橄榄绿(olive), 思想(#think)标题为绿色(green)，生活(#life)标题为橘色(orange)。

```css
#chosen {
      color: red;
    }
    #news {
      color: blue;
    }
    #finance {
      color: olive;
    }
    #think {
      color: green;
    }
    #life {
      color: orange;
    }
    

    /*选择menu元素下的li子元素*/
    #menu li {
      float: left;
      width: 70px;
      font-size: 1.2em;
      font-weight: lighter;
    }
    /*选择menu元素下的li子元素和li下得a子元素*/
    #menu li, li a {
      list-style: none;
      text-decoration: none;
    }
```

```html
<header id="menu">
```