# 第1关：while类型

## 求出小于等于整数a的所有质数；计算并返回所有这些质数的和；
```javascript
if (a < 2) { return 0 }
var sum = 0;
for (var i = 2; i <= a; i++) {
    if (judge(i)) { sum += i }
}
return sum;
```


# 第2关：do while类型

## 求出并返回参数a和b之间的所有整数的和，不包括这两个端点；

```javascript
if (b - a < 2) return 0;
var sum = 0;
var i = a + 1;
do {
    sum += i;
    i++;
} while (i < b);
return sum;
```


# 第3关：for类型

## 计算并返回整数a的“倒数”；

```javascript
var tmp = 0;
var result = 0;
while (Math.floor(a / 10) > 0) {
    tmp = a % 10;
    result = result * 10 + tmp;
    a = Math.floor(a / 10);
}
return result * 10 + a;
```


# 第4关：for in类型

## 平台将读取用户补全后的ForInFunction.js；调用其中的mainJs()方法，并生成若干组测试数据；

```javascript
var r = '';
for (const p in apple) {
    if (p.indexOf("location") != -1) {
        r += apple[p];
    }
}
return r;
```


# 第5关：break和continue的区别——break

## 平台将读取用户补全后的BreakContinue；调用其中的mainJs()方法，并生成若干组测试数据；
```javascript
    for (var p = 0; p < arr.length; p++) {
        if (judge(arr[p]) == true) {
            return arr[p];
        }
    }
```


# 第6关：break和continue的区别——continue

## a是一个数字数组，b是非零整数；如果b为正数，计算a中所有正数的和；如果b是负数，计算a中所有负数的和；

```javascript
if (b > 0 && a[i] < 0) {
    continue;
} else if (b < 0 && a[i] > 0) {
    continue;
}
```