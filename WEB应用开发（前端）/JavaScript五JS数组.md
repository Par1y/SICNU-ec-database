# 第1关：数组的创建、读写和长度

## 已知两个数组array1和array2，参数a是一个整数，先判断a的值与数组array1的长度值相等，如果相等，返回数组array1的最后一个元素，反之，则返回数组array2的最后一个元素；

```javascript
if (a == array1.length) return array1[a-1];
else return array2[array2.length-1];
```


# 第2关：数组元素的增减

## 将数组testArray的最后a个元素移动到最前面，这a个元素之间的相对位置不变，其余元素之间的相对位置不变；比如将数组[1,2,3,4,5]最后2个元素移动到最前面，数组变为[4,5,1,2,3]；返回移动结束后数组在索引b处的元素；

```javascript
var lastElements = testArray.splice(-a, a);
Array.prototype.unshift.apply(testArray, lastElements);
return testArray[b];
```


# 第3关：数组的遍历和多维数组

## 将一维数组arr转为a行b列的二维数组，行优先；返回该二维数组；

```javascript
var tarr = new Array(a);
for (var i = 0; i < a; i++) {
    tarr[i] = new Array(b);
}

for (var i = 0; i < a; i++) {
    for (var j = 0; j < b; j++) {
        tarr[i][j] = arr[i * b + j];
    }
}
return tarr;
```


# 第4关：数组的常用方法

获取字符串a在数组myArray的所有位置并组成一个位置数组；获取字符串b在数组myArray的所有位置并组成一个位置数组；合并这两个数组然后返回合并后的数组。

```javascript
function findArr(t) {
    var rarr = [];
    var i = 0;
    var n = myArray.indexOf(t, i); // 查找起始位置
    while (n!== -1) { // 当找到元素时继续循环
        rarr.push(n);
        i = n + 1; // 下一次从下个位置开始查找
        n = myArray.indexOf(t, i);
    }
    return rarr; // 返回结果数组
}
var aarr = findArr("a");
var barr = findArr("b");
return aarr.concat(barr); // 合并两个索引数组
```


# 第5关：数组的应用——内排序

## 函数mainJs(a)中的变量arr是一个数组，你需要对该数组进行选择排序；返回选择排序进行过程中，在每一趟交换前，待排序子数组的最大元素的位置组成的数组；比如对于上面相关知识中的数组[9,5,8,0,2,6]，第一次交换前，最大的元素9的索引是0，第二次交换前，最大元素8的索引是2，第三次交换前最大元素6的索引是0，第四次交换前最大元素5的索引是1，第五次交换前最大元素2的索引是1，第六次交换前最大元素0的索引是0。索引需要返回的数组是[0,2,0,1,1,0]；

```javascript
var result = [];
const n = arr.length;
for (let i = 0; i < n-1; i++) {
    const currentEndIndex = n - 1 - i;
    let maxIndex = 0;
    for (let j = 0; j <= currentEndIndex; j++) {
        if (arr[j] > arr[maxIndex]) {
            maxIndex = j;
        }
    }
    result.push(maxIndex);
    [arr[maxIndex], arr[currentEndIndex]] = [arr[currentEndIndex], arr[maxIndex]];
}
return result;
```