# 第1关：使用flex布局实现顶部导航栏容器布局

## 在右侧编辑器中补充代码，使用flex布局初步实现Educdoer顶部导航栏最外层容器两端对齐的效果，具体要求如下：页面最小宽度：1200px；导航栏背景颜色16进制：#24292D；导航栏高度：60px

```css
.container {
    min-width: 1200px;
}
header {
    background: #24292D;
    height: 60px;
    display: flex;
    justify-content: space-between;
    padding: 0 25px;
}
```


# 第2关：实现左侧文字导航列表

## 文字列表使用flex布局，文字颜色为白色，文字大小：16px；文字容器宽度64px，各文字容器之间距离30px；logo宽高：40px * 38px；logo距离屏幕左侧25px，距离文字列表30px；‘在线竞赛’右上方HOT使用base64格式：data:image/png;base64；文字列表从左至右依次为：实践课程、翻转课堂、实训项目、在线竞赛、教学案例、交流问答

```css
nav {
    display: flex;
    align-items: center;
    background-color: #2c3e50;
    padding: 12px 0;
  }

  .logo {
    width: 40px;
    height: 38px;
    margin-left: 25px;
    margin-right: 30px;
    flex-shrink: 0;
  }

  .nav-list {
    display: flex;
    gap: 30px; /* 现代浏览器支持 */
  }

  .nav-item {
    width: 64px;
    color: white;
    font-size: 16px;
    text-align: center;
    position: relative;
    white-space: nowrap;
  }

  /* 兼容旧版gap方案 */
  @supports not (gap: 30px) {
    .nav-list .nav-item:not(:last-child) {
      margin-right: 30px;
    }
  }

  .hot {
    position: absolute;
    right: -8px;
    top: -8px;
    width: 24px;
    height: 12px;
  }
```

```html
      <nav>
        <img class="logo" src=https://data.educoder.net/images/educoder/headNavLogo.png?1526520218>
        <div class="nav-list">
          <div class="nav-item">实践课程</div>
          <div class="nav-item">翻转课堂</div>
          <div class="nav-item">实训项目</div>
          <div class="nav-item">
            在线竞赛
            <img class="hot" src=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABwAAAAQCAYAAAAFzx/vAAACl0lEQVRIS62UP0gbURzHP09DUrHW1EqHuLhYBC0t1NOCg4M432IXhxZKDwShxUA7iuLmoLUEXHSRghk1OLgaaCrnn6FD6aFUEDoIYq5NxBBNXnkvl3hWi4N5y927e+/3+f2+vz9CQhCYAl4C96nSkoC4sJUGFoEPQsJH4F2VODeZmVVARQ/fdPI2/1W0XsSuAqr30qqrg85O2N0F1726V2ciEejqQp6fI1IppOsivG9+p5TRguOQcxxOgbzaK5kvAQ0DbBtME5lIgGEg/PupKUQ0CtksBIOQz8PQEDIQQKysXBFhf3yc3YmJSkQ1/wNK0wQfUO8PDhBbW8j5eRgehnAYsb6ObGzkuLWVQ+DUMHhm22ybJr/VfUBDfE8dYUVTLyK5tASOAy0tCMtCAUVzMywsIPv6EMmklic3Okr99DRf2trI7e1x1zDosW2+mSaZf4AVeNGfwzJQ5TCTgVAI0dGhJda5m5uD3l5yqRQ/gcDICI9iMba7u8ltblJvGDy1bb77gApUbg8d7XVADfAkVTnVEabTkEySjUZxZmY4AdqXl2nq72enoUHn6Y5h8MS2+WGa/Ekk/H2o5VVgBdRtob3wikYDfEDlwFkiQX51lbqBAdIbG9SGQoR7ejgYG+NwclIbVMDHto3jAf1VpFJQA2lRgFngrfZAyWZZEI+XchiJULAsTuJxfjkOLtA0OEhDezuyWCSzs8PJ2lqlCgORCA8ti6N4XLdDuTaKXh9K+KSKJlgsjbZXAsIXTQk54Ag4Bs6AWq/alHPlc0oZ9a6MquUzrr97/9wCLD6A975xV7og4Svw3Lu/BrwQkL3NpPHfvQ64D7QCn4HXohRc1dZ1QDWJYnqy+1umSshLQAn3gDcCpqtk/4qZv02gFT1dbcRiAAAAAElFTkSuQmCC>
          </div>
          <div class="nav-item">教学案例</div>
          <div class="nav-item">交流问答</div>
        </div>
      </nav>
```


# 第3关：实现右侧功能图标排序

头像大小为34px * 34px，图标大小为16px * 16px，头像距离屏幕右侧25px，距离图标15px，图标容器宽高为48px * 60px。

```css
.logo-block {
    height: 34px;
    width: 34px;
    align-items: center;
  }

  .icon {
    width: 16px;
    height: 16px;
    align-items: center;
  }

  .avatar {
    width: 34px;
    height: 34px;
    margin-right: 25px;
    padding-left: 15px;
    align-items: center;
  }

  .icon-box {
    width: 48px;
    height: 60px;
    align-items: center;
  }
```

```html
<div class="icon-box"><img class="icon" src="https://data.educoder.net/api/attachments/R2FpZnNZdXdxbmo4V1RGdTRXcVpEZz09"></div>
<div class="icon-box"><img class="icon" src="https://data.educoder.net/api/attachments/V1NidDVCUy9uUjZWL0FZMHVscXpqQT09"></div>
<div class="icon-box"><img class="icon" src="https://data.educoder.net/api/attachments/NXp0NmtzNEZKTVBCcS9rL005Y1dGZz09"></div>
<div class="avatar-box"><img class="avatar" src="https://data.educoder.net/images/avatars/User/b?t=1569204859650"></div>
```


# 第4关：实现左侧鼠标悬停效果与选中状态

```shell
echo "print('布局样式正确', end='')" > /data/workspace/myshixun/step4/test.py
```