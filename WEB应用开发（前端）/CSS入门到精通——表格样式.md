# 第1关：表格边框

## 设置表格为折叠边框；设置Table属性边框为2px粗的黑色(black)实线；设置th属性边框为1px粗的灰色(grey)实线；设置td属性边框为1px粗的灰色(grey)点线。

```css
border-collapse: collapse;
border: 2px solid black;
th {
    border: 1px solid grey;
}
td {
    border: 1px dotted grey;
}
```


# 第2关：表格颜色、文字与大小

## 设置标题(caption)字体为20px大小的粗体，高度为40px；设置th、td共同属性。单元格大小的高度为50px，宽度为100px；字体样式设置为居中；修改th边框为白色；设置th背景色为lightseagreen，设置th字体颜色为白色。

```javascript
font-weight: bold;
height: 40px;
font-size: 20px;
height: 50px;
width: 100px;
text-align: center;
border: 1px solid white;
background-color: lightseagreen;
color: white;
```