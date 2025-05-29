# 第1关：jQuery动画效果——隐藏/显示

## 点击隐藏按钮，橙色小框消失，速度为slow，完成后弹出我隐藏了；点击显示按钮，橙色小框显示，速度为"1s，完成后弹出我显示了；点击toggle按钮，第一次点击，橙色小框隐藏显示；第二次点击，橙色小框显示隐藏。效果来回切换，速度为"fast，完成后弹出隐藏显示的切换。

    $(".hide").click(function(){
        $(".item").hide("slow",function(){alert("我隐藏了");});
    });
    $(".show").click(function(){
        $(".item").show(1000,function(){alert("我显示了");});
    });
    $(".toggle").click(function(){
        $(".item").toggle("fast",function(){alert("隐藏显示的切换");});
    });


# 第2关：jQuery动画效果——淡入淡出

## 点击【动画开始】按钮，第一张图片透明度从1变为0.5，速度为2s；第二张图片在延迟2s后，透明度也从1变为0.5，速度为2s；两张图片一起淡出，速度为"slow"。

    $(".first").fadeTo(2000,0.5);
    $(".second").delay(2000).fadeTo(2000,0.5);
    $(".first").delay(2000).fadeOut("slow");
    $(".second").fadeOut("slow");


# 第3关：jQuery动画效果——滑动

## 当鼠标浮动到菜单时， 菜单内容向下滑动，速度为1s；当鼠标离开菜单时， 菜单内容向上滑动，速度为1s。

    $(".menu").mouseenter(function(){
        $(".list").slideDown(1000);
    });
    $(".menu").mouseleave(function(){
        $(".list").slideUp(1000);
    });


# 第4关：jQuery动画效果——自定义动画

## 当点击【点赞】按钮时，爱心立即显示；然后爱心向上移动 120px（用相对值），同时透明度变为0，速度为1.5s。

    $(".love").show().animate({top:"-=120px", opacity:"0"}, 1500);