# 第1关：jQuery入门

## 用 jQuery 获取到 id="content"的div；div里面的内容为 这是我的第一个jquery程序。

    $("#content").html("这是我的第一个jquery程序");


# 第2关：jQuery基本选择器

## 用id选择器，获取id="box"的div，添加内容为我是id选择器添加的内容；用类选择器，获取class="box"的div，添加内容为我是类选择器添加的内容；用元素选择器，获取 p 标签，添加内容为我是元素选择器添加的内容。

    $("#box").html("我是id选择器添加的内容");

    $(".box").html("我是类选择器添加的内容");

    $("p").html("我是元素选择器添加的内容");


# 第3关：过滤选择器 （一）

## 用过滤选择器获取要操作的DOM元素；设置表头颜色为 yellowgreen；设置奇数行颜色为  lightyellow；设置偶数行颜色为  lavenderblush；

    $("tr:odd").css("background","lightyellow");
    $("tr:even").css("background","lavenderblush");
    $("tr:first").css("background","yellowgreen");


# 第4关：过滤选择器 （二）

## 用选择器实现下面的效果，相应的方法可以在平台上自行调试；选取第三行，填充背景色为"#eee"；除了最后一行，其他都要底边边框，边框样式为：1px dashed #ccc。

    $(".item:eq(2)").css("background", "#eee"); 
    $(".item:not(:last)").css("border-bottom","1px dashed #ccc");


# 第5关：tab选项卡

## 当点击上面的tab选项卡时，下面会显示对应的内容，添加的类为active；tab切换静态页面已经写好，初始化已经完成，只需完成切换的功能；

    $(".head li").removeClass("active").eq(index).addClass("active");
    $(".content div").hide().eq(index).show();