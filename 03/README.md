## Canvas:  笔画和填充


在 Canvas 上画线时有两个属性需要设置

    1.Stroke 笔画

    2. Fill 填充颜色

笔画和填充颜色决定了如何绘制形状， Stroke绘制图形的外边框， 而fill 填充图形内部的


```js
 window.onload = ()=>{
        drawExamples()
    }
    function drawExamples(){
        //获得canvas实例
        var canvas = document.getElementById('k-canvas')
        var context = canvas.getContext("2d")

        //设置填充样式并绘制一个方形
        context.fillStyle = "#009900"
        context.fillRect(10,10, 100, 100);

        //设置方形的边框宽度和颜色
        context.strokeStyle = "#0000ff";
        context.lineWidth =5;
        context.strokeRect(10,10,100,100);
    }
```