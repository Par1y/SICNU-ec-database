# 第1关：if-else类型

## 根据分数a（百分制）返回考试结果；本题考察非嵌套的if-else语句；

```javascript
if (a < 60) return 'unpass';
else return 'pass';
```


# 第2关：switch类型

## 根据面积参数a返回湖泊的名字，湖泊的名称和面积的对照表在最上面的任务描述里面，这里不再赘述；没有对应的湖泊返回error；

```javascript
switch (a) {
        case 82414: return "Superior";
        case 59600: return "Huron";
        case 58016: return "Michigan";
        case 25744: return "Erie";
        case 19554: return "Ontario";
        default: return "error";
    }
```


# 第3关：综合练习

## 完成函数judgeLeapYear(year)，功能是判断某一年是否为闰年，是则返回“xxx年是闰年”，否则返回“xxx年不是闰年”。参数year是表示年份的四位数整数。

```javascript
if (year % 100 != 0 && year % 4 != 0) return year + "年不是闰年";
    else if (year % 100 == 0 && year % 400 != 0) return year + "年不是闰年";
    else return year + "年是闰年";
```

## 完成函数normalizeInput(input)，功能是对输入的字符串进行规范化，参数input是输入的字符串，返回规范化后的字符串，规范化的标准如下：

| input | 输出 |
|---|---|
| 中共党员 | 中共党员 |
| 党员 | 中共党员 |
| 共产党员 | 中共党员 |
| 中共预备党员 | 中共预备党员 |
| 预备党员 | 中共预备党员 |
| 团员 | 共青团员 |
| 共青团员 | 共青团员 |
| 大众 | 群众 |
| 群众 | 群众 |
| 市民 | 群众 |
| 人民 | 群众 |
| （其他数据） | 错误数据 |

```javascript
function normalizeInput(input) {
    const mapping = {
        '中共党员': '中共党员',
        '党员': '中共党员',
        '共产党员': '中共党员',
        '中共预备党员': '中共预备党员',
        '预备党员': '中共预备党员',
        '团员': '共青团员',
        '共青团员': '共青团员',
        '大众': '群众',
        '群众': '群众',
        '市民': '群众',
        '人民': '群众'
    };
    return mapping[input] || '错误数据';
}
```

## 完成函数evaluateApple(weight,water)，功能是判断苹果是否为优质品，是则返回“是优质品”，否则返回“不是优质品”。参数weight表示重量（克），为整数；参数water表示含水量，为小数。

判断标准如下：

weight大于等于200，为优质品；
weight小于200，但water大于等于0.7为优质品；
其余不是优质品。
效果如下：
weight为220，water为0.6，返回“是优质品”。

```javascript
if (weight < 200 && water < 0.7) return "不是优质品";
else return "是优质品";
```