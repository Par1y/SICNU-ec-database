# 第1关：JSON对象

## 定义一个JSON对象JSONObject，它有三个属性：key1、key2和key3，它们的值分别是参数a、b和c；删除其中名字为key3的属性；删除完成后，遍历其余的所有属性，返回各属性的值连接成的字符串，中间用,隔开；

    var JSONObject = { "key1":a, "key2":b, "key3":c}
    delete JSONObject.key3
    var str = ""
    for (att in JSONObject) {
        str += JSONObject[att]
        if (att == 'key1') {
            str += ','
        }
    }
    return str


# 第2关：JSON数组

## 已知myJson的第三个属性的值是一个数组，参数a是一个数字，要求将数组中前a个元素（这些元素都是字符串类型）拼接起来，元素之间用,隔开，返回拼接后的字符串；

    var t = myJson.language;
    var r = ""
    for (var i = 0; i < a; i++) {
        r += t[i]
        if (i < a - 1) {
            r += ","
        }
    }
    return r


# 第3关：JSON字符串

## 先将JSON字符串JSONString转换为JavaScript对象JSONObject；然后将JSONObject的key1属性的值设置为mainJs()函数的参数a；最后将JSONObject转换为JSON字符串，并返回该字符串；

    var JSONObject = JSON.parse(JSONString)
    JSONObject.key1 = a
    return JSON.stringify(JSONObject)