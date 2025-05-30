# 第1关：用函数语句定义函数

## 定义一个名字为mainJs()的函数；该函数有两个参数，均为字符串类型；函数的功能是返回这两个参数的拼接结果；

    function mainJs(arg1, arg2) {
        return arg1 + arg2;
    }


# 第2关：用表达式定义函数

## 定义一个匿名函数，将它赋值给变量myFunc；该函数实现求一个三位数的各个位上的数字之和，比如123各个位上的数字分别为1、2和3，和是6；

    var myFunc = function (n) {
        var sum = 0;
        for (var i = 0; i < 3; i++){
            sum += n % 10;
            n = Math.floor(n / 10);
        }
        return sum;
    };


# 第3关：函数的调用

## mainJs()代码区上面定义了三个函数，从上到下分别编号为1、2和3；mainJs()有三个参数a、b和c，根据a的值（函数的编号，可取的值是1、2和3）调用相应的函数（可选的函数分别是getMax()、getMin()和getSum()，具体请参考代码！），并传入参数b和c，返回得到的结果；比如a为1表示你需要调用函数getMax()；

    if (a == 1) {
        return getMax(b, c);
    } else if (a == 2) {
        return getMin(b, c);
    } else {
        return myObject.myFunc(b, c);
    }


# 第4关：未定义的实参

## 路口有四个方向的红绿灯，其默认值分别是green、green、red和yellow；对于函数mainJs(a,b,c,d)的四个参数，要求在没有传入实参或者传入undefined时，其分别设置为上述默认值；最后返回四个字符串型参数的拼接结果，字符串中间用-符号隔开，如分别传入red、red、yellow和undefined时，返回red-red-yellow-yellow；

    ra = 'green';
    rb = 'green';
    rc = 'red';
    rd = 'yellow';
    if (a != undefined) { ra = a; }
    if (b != undefined) { rb = b; }
    if (c != undefined) { rc = c; }
    if (d != undefined) { rd = d; }
    return ra + '-' + rb + '-' + rc + '-' + rd;


# 第5关：实参对象

## 定义函数getMax()；该函数计算并返回一组整数的最大值；整数的个数不确定；如果整数个数为0，直接返回0；

    function getMax() {
        if (arguments.length == 0) return 0;
        var max = arguments[0];
        for (var i = 1; i < arguments.length; i++) {
            if (arguments[i] > max) max = arguments[i];
        }
        return max;
    }


# 第6关：对象作为参数

## 函数objcetFunction()的参数是一个对象，该函数的功能是返回属性名1+':'+属性值1+','+属性名2+':'+属性值2+','+......+属性值n+','；测试的时候我们会往mainJs()传入参数1或2或3，分别表示调用函数objectFunction()并传入对象参数park、computer或者city；比如对于第一个对象park，该函数需要返回name:Leaf Prak,location:Fifth Avenue,todayTourists:4000,；

    let result = '';
    for (const key in object) {
        if (object.hasOwnProperty(key)) {
            result += key + ':' + object[key] + ',';
        }
    }
    return result;


# 第7关：函数对象

## 已知`getOddNumber(a)`求数组`a`中奇元素的个数，`getEvenNumber(a)`求数组`a`中偶元素的个数；完成函数`getNumber(func,a)`，实现：根据函数参数`func`的不同，求数组`a`中奇元素的个数或者偶元素的个数；

    return func(a);