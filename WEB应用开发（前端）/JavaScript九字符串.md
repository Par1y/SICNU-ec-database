# 第1关：查找字符串的位置

## 函数mainJs()有两个字符串参数a和b，其中b比较短；要求将b从左到右在a中查找，返回查找的位置之和；比如a为ababab，b为ab，b在三个地方与a的子串查找，位置分别是0、2和4，返回他们的和6；

    var i = 0;
    var sum = 0;
    while (i < a.length - b.length) {
        var tmp = a.indexOf(b,i+1);
        if (tmp != -1) {
            i = tmp;
            sum += tmp;
        } else {
            break;
        }
    }
    return sum;


# 第2关：求指定位置的字符

## mainJs()的参数a是一个身份证号，要求返回其中的前六位；

    return a.substr(0, 6);


# 第3关：字符串的截取

## 参数a表示待处理的碱基对序列，参数b表示可能的杂质字符串，a中只混入了0个或者1个杂质b，无其它杂质字符串；你需要删除杂质b，返回无杂质的a碱基对；

    var r = '';
    var i = 0;
    while (i <= a.length - b.length) {
        if (a.substr(i, b.length) === b) {
            r += a.substring(0, i);
            a = a.substring(i + b.length);
            i = 0;
        } else {
            i++;
        }
    }
    r += a;
    return r;


# 第4关：大小写转换

## 已知参数a和b都是字符串，a比b长；要求找到a中所有与b匹配的子字符串，将这些子字符串全部转化为大写，a的其它部分不变，返回转化完成后的a；

    var i = 0;
    while (i < a.length - b.length) {
        var tmp = a.indexOf(b,i);
        if (tmp != -1) {
            var mid = a.substring(0, tmp);
            mid += b.toUpperCase();
            mid += a.substring(tmp + b.length);
            a = mid;
            i = tmp + 1;
        } else {
            return a;
        }
    }
    return a;


# 第5关：字符串的分割

## 参数a是字符串，是一段英文的文本，单词与单词之间要么以,隔开，要么以空格字符（即键盘上的spcae键）隔开；利用split()方法统计a中单词的个数；

    var w = [];
    w = a.split(/[, ]+/gm);
    return w.length;