
## Canvas Overview

本章节提供 canvas 的基础用法。 分为两部分

1. 声明一个 Canvas 元素
2. 在该元素上绘制图形

>声明一个画布元素

首先我们看一下如何在html中声明一个画布

```[html]
<canvas id="c-canvas" width="500" height="500" style="border:1px solid #cccccc;">
    HTML5 Canvas not supported
</canvas>
````

上面的代码声明了一个宽度为500，高度150， 并设置边框样式，

canvas 标签内部的组建可以忽略掉，当浏览器不支持 canvas 时，浏览器才会显示。

## 使用 Canvas画图

Canvas是实时绘制。 意味着只要你在画布上了绘制了一个形状，画布就不再知道盖形状的信息。 而图形会被及时显示出来。你无法操作该图形。

与SVG相反， 在SVG中，你可以单独操作形状，并重新绘制整个图标， 在THML中，如果要更改绘制的图形，则必须要重新绘制所有内容。

在Canvas上绘制需要使用Javascript，可以按照一下步骤尝试：

1. 等待页面完全加载
2. 获得 canvas 实例
3. 获得 2D 上下文
4. 使用 2D 上下文绘制内容


```js
window.onload =function(){
    drawText()
}

function drawText(){
    let canvas = document.getElementById("k-canvas")
    let context = canvas.getContext("2d")

    context.fillStyle = "#ff0000";
    context.fillRect(10, 10, 100, 100);
}
```