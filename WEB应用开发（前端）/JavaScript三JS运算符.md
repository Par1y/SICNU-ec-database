## 第1关：算术运算符

## 完成函数mainJs()；将两个字符串参数a和b转换为数字；计算a除以b的余数c；将a、b、c分别转换为字符串；拼接字符串a、b和c；

```javascript
ta = parseInt(a);
tb = parseInt(b);
tc = ta % tb;
c = String(tc);
```


# 第2关：比较和逻辑运算符

## 完成函数mainJs()；比较字符串a和b的大小；如果a>b，则返回a逻辑与b的结果，否则返回a逻辑取反的结果（返回时使用return）；

```javascript
if (a > b) return a && b; else return !b;
```


# 第3关：条件和赋值运算符

## 完成函数mainJs()；返回参数a和b中较大的字符串；

```javascript
if (a > b) return a; else return b;
```


# 第4关：运算符的优先级和结合性

## 参数a先减去1,所得差再与参数b相加，然后将结果再与b相乘；上面的结果为24则给参数c赋值1，否则赋值0；计算c与d（d等于4）的积，这个积再与参数d求和，所得结果赋值给参数e；

```javascript
var c = (--a + b) * b;
c = c == 24 ? 1 : 0;
var d = 4
var e = c * d + d;
```