# 第1关：JavaScript 数据类型介绍

## 在函数objectTest()内部定义了六个变量a、b、c、d、e、f并已赋值，需判断它们各是什么数据类型；变量aType、bType、cType、dType、eType、fType分别表示上面六个变量的数据类型的名字，需给它们赋值，可选的数据类型名如下：number、string、bool、object、undefined和array分别表示数字、字符串、布尔型、对象类型、undefined还有数组。

```javascript
aType = "object";
bType = "array";
cType = "number";
dType = "string";
eType = "bool";
fType = "undefined";
```


# 第2关：JavaScript 数据类型转换

## 完成函数 `mainJs()`，把函数三个参数（从左到右）依次转换为整数，整数和小数。第一个参数既有可能是 12 这种纯整数的字符串形式，也有可能是 12a3 这种含有非数字字符的字符串；第二个参数是 16 进制数字的字符串形式，如 af2；第三个参数是纯小数的字符串形式，如 12.2。

```javascript
var a = parseInt(args1);
var b = parseInt(args2,16);
var c = parseFloat(args3);
```