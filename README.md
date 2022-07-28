# front-end-notes
前端笔记

##  1. vw、vh


    vw： 视窗宽度的百分比（1vw 代表视窗的宽度为 1%）
    vh： 视窗高度的百分比（ 1vh 代表视窗的高度为 1%）
    vmin：当前 vw 和 vh 中较小的一个值
    vmax：当前 vw 和 vh 中较大的一个值
    vw、vh与 % 的区别：

    % 是相对于父元素的大小设定的比率，vw、vh 是视窗大小决定的。
    vw、vh 优势在于能够直接获取高度，而用 % 在没有设置 body高度的情况下，是无法正确获得可视区域的高度的，所以这是挺不错的优势。
    ————————————————
    版权声明：本文为CSDN博主「全易」的原创文章，遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接及本声明。
    原文链接：https://blog.csdn.net/qq_42618566/article/details/101752942




## input[type=number]下禁止输入e、+、-的解决方案

```html
    onKeypress="return (/[\d]/.test(String.fromCharCode(event.keyCode)))" 

    <input v-model="goPage"
    onKeypress="return (/[\d]/.test(String.fromCharCode(event.keyCode)))" 
    :max="9999999" type="number" placeholder="请输入"></input>
            

```
