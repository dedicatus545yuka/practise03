# practise03
有关背景图和导航条的一点练习  
### 说真的这也折腾了我不少时间了，总算是有模有样，当然我对这代码不是很满意，如果是今天写的话可能会实现的更容易些吧  
PS 这算是补发的  
```HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>导条实例</title>
    <link rel="stylesheet" href="导条实例.css">
</head>
<body>
<div>
    <ul>
        <li class=""><a href="#"></a></li>
        <li class=""><a href="#"></a></li>
        <li class=""><a href="#"></a></li>
    </ul>
    <!-- 页面主体是一个盒子包住一个无序列表 -->
    <span></span>
    <!-- 这里是为了给阴影一个容器 -->
</div>
</body>
</html>
```

`导条实例.css`

```CSS
body {
    margin: 0px;
}
/* 解决页面默认8像素的问题 */
div {
    width: 100%;
    float: left;
    /* 浮动是为了解决高度塌陷的问题 */
    position: absolute;
    top: -5px;
    /* 设置一些偏移量起到控制阴影位置的效果*/
}
a {
    background-image: url(http://a1.qpic.cn/psb?/V118JuTr3rHMrA/CXubb72btii0m7CVU.6YGLiIEK1d0GV570m0nQBzyQk!/b/dPMAAAAAAAAA&bo=FwEdAAAAAAADAC4!&rf=viewer_4);
    width: 93px;
    height: 29px;
    /* 给a标签设置一个背景图片并且给与它与图片相同的高度宽度*/
    background-repeat: no-repeat;
    /* 设置图片的平铺方式 */
    float: left;
}
a:hover{
    background-position: -93px 0;
    /* 设置背景图片的起始位置 */
}
a:active {
    background-position: -186px 0;
}
/* 给元素设置伪类 */
li {
    float: left;
    padding: 10px;
    /* 设置内边距可以起到让元素居中的效果并且拉开兄弟元素之间的间隙 */
    display: inline-block;
    /* 让元素显示为行内块级元素可隐藏列表前的黑点*/
    margin-right: -6px;
    margin-bottom: -20px;
}
ul {
    width: 400px;
    margin: auto;
    position: relative;
    /* 让列表可以在盒子内居中 */
}
span {
    position: absolute;
    left: 0px;
    bottom: -32px;
    width: 100%;
    height: 32px;
    _display: none;
    background: url(http://a3.qpic.cn/psb?/V118JuTr3rHMrA/R20YssnJ9G3nxRyuN6NnzAP.aVmylL9LFj4aUA.FZYk!/m/dPIAAAAAAAAA&bo=jQUgAAAAAAADB4o!&rf=photolist) no-repeat center bottom;
}
/* 给盒子设置阴影效果 */
```
### 顺带附上页面的显示效果图吧
！[效果图](http://a2.qpic.cn/psb?/V118JuTr3rHMrA/8TOJoqrQHPayQEzb..bRMvmOJ891LmNywYZMRhVBPpA!/b/dD8BAAAAAAAA&bo=PgsKAQAAAAADABs!&rf=viewer_4)
