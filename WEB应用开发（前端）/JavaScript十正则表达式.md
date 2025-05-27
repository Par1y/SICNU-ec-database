# 第1关：字符串字面量

## 定义正则表达式pattern；pattern匹配字符串js后面紧跟换行符的这样一类字符串；

    var pattern = /js\n/;


# 第2关：字符类

## 定义正则表达式pattern1和pattern2；pattern1用来匹配一个英文字母后面紧跟一个数字；pattern2用来匹配字母A后面紧跟一个非数字的字符；

    var pattern1 = /[a-zA-Z]\d/;
    var pattern2 = /A\D/;


# 第3关：重复

## 定义正则表达式pattern1、pattern2、pattern3、pattern4；pattern1匹配这样一类字符串：?至少出现一次；pattern2匹配这样一类字符串：+只出现三次；pattern3匹配这样一类字符串：{}最少出现一次，最多出现两次；pattern4匹配这样一类字符串：\出现一次或者不出现；

    var pattern1 = /\?+/;
    var pattern2 = /\+{3}/;
    var pattern3 = /{}{1,2}/;
    var pattern4 = /\\?/;


# 第4关：选择

## 定义正则表达式pattern1、pattern2和pattern3；pattern1用来匹配一段含有身份证号码的字符串，身份证号的规律是：17位数字，加上1位数字或者大写字母X；pattern2用来匹配一段含有某地的邮编的字符串，邮编的规律是：23或者24再加4位数字；pattern3用来匹配一段含有三位数电话区号的字符串，三位数电话区号只有10个，它们分别是010、020、021、022、023、024、025、027、028、029；

    var pattern1 = /\d{17}(\d|X)/;
    var pattern2 = /2[3|4](\d){4}/;
    var pattern3 = /010|02[0|1|2|3|4|5|7|8|9]/;


# 第5关：分组

## 创建正则表达式pattern1，匹配这样的字符串：?+需要连续出现至少两次；创建正则表达式pattern2，匹配这样的字符串：数字+问号+数字，或者数字+加号+数字，比如1?1、1+4、asd0+3asdfa;

    var pattern1 = /(\?\+){2,}/;
    var pattern2 = /(\d\?\d)|(\d\+\d)/;


# 第6关：引用

## 创建正则表达式pattern1，匹配这样的字符串：三个数字加一个非数字字符再加三个数字，字符两侧的数字相同，如123A123、234,234；创建正则表达式pattern2，匹配这样的字符串：大写字母+数字+大写字母+数字+大写字母+数字，三个数字相同，如A2B2C2、F9D9K9；

    var pattern1 = /(\d\d\d)\D\1/;
    var pattern2 = /[A-Z](\d)[A-Z]\1[A-Z]\1/;


# 第7关：匹配位置

## 定义正则表达式pattern；pattern匹配以单词js开头的一段文本：这段文本以js开头，且这个js是一个单词，比如js is good、js's history符合要求，而js2、jsjs不符合要求；

    var pattern = /^js\b/;


# 第8关：修饰符

## 定义正则表达式pattern；pattern能够匹配一段英文中所有的单词shell，不区分大小写，该段英文在一行中；所谓单词，指前后紧跟的字符都不是英文字母的字符串；

    var pattern = /\bshell\b/gi;


# 第9关：正则表达式的使用

## 一段成绩单是类似这样的字符串：Sivan:99,Kathy:100,Eray:8,，即：人名+冒号+成绩+逗号，成绩范围是0到100，人名是英文；使用replace()方法删掉其中的分数，保留其他所有字符串，比如上面的最终结果应该是Sivan:,Kathy:,Eray:,；

    var pat = /100|([0-9][0-9]|[0-9])/g;
    return a.replace(pat, "");