# 第1关：对象的创建

## 使用对象字面量方法创建名为student的对象，有两个属性name和gender，他们的值分别是mainJs()函数的参数a和参数b；使用已给的构造函数Car(plate,owner)创建一个对象myCar，它的两个属性的值分别是参数c和参数d；使用原型创建一个对象myJob，它的构造函数是Job(company,salary)，它的两个属性的值已经被设置，你需要用参数e覆盖属性company的值；

```javascript
var student = new Object();
student.name = a;
student.gender = b;

var myCar = new Car(c, d);

var myJob = new Job();
myJob.company = e;
```


## 第2关：属性的增删改查

如果调用函数reviseAttribute（reviser,date,attvalue）并传入值 Alice,1,1000那么对应store的day1属性的值就修改为1000,accountant属性的值修改为Alice；

```javascript
store.accountant = reviser;
store['day' + date] = attValue;
```


# 第3关：属性的检测和枚举

## 有两个可选的对象orange和car，判断给定的属性名a属于哪一个对象；返回该对象的所有自有属性名组成的字符串，例如：如果判断为car，则返回brandpricemodel；

```javascript
var result = '';
    if (orange.hasOwnProperty(a)) {
        for (const key in orange) {
            result += key;
        }
    } else if (car.hasOwnProperty(a)) {
        for (const key in car) {
            result += key;
        }
    }
    return result;
```