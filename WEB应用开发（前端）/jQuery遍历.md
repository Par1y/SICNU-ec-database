# 第1关：jQuery——遍历DOM元素的祖先元素

## 本关操作的元素是p元素；设置div元素的背景色为#fff；设置body元素的背景色为#ccc。

    $(".item").parent().css("background","#fff");
    $(".item").parents().css("background", "#ccc");


# 第2关：jQuery——遍历DOM元素的后代元素

## 本关操作的元素是div元素；设置p元素的背景色为red；设置span元素的字体颜色为#fff。

    $(".container").children().css("background","red");
    $(".container").find(".item").css("color","#fff");


# 第3关：jQuery——遍历DOM元素的兄弟元素

## 这里只用siblings(), pre(), prevAll(), next() 来实现下面效果，注意使用的先后顺序，因为颜色会覆盖；设置p元素的颜色为red；设置span元素的颜色为orange；设置ul元素的颜色为green；设置ol元素的颜色为cyan。

    $(".item").siblings().css("background","cyan");
    $(".item").prevAll().css("background","red");
    $(".item").prev().css("background","orange");
    $(".item").next().css("background","green");


# 第4关：jQuery遍历——过滤

## 获取第一个p元素，改变字体颜色为red；获取匹配class="active"的p元素，改变字体颜色为orange；获取第三个p元素，改变字体颜色为yellow；获取没有class="item"的p元素，改变字体颜色为green；获取最后一个p元素，改变字体颜色为blue。

    $(".item").first().css("color","red");
    $(".item").filter(".active").css("color","orange");
    $(".item").eq(2).css("color","yellow");
    $(".four").not(".item").css("color","green");
    $(".item").last().css("color","blue");