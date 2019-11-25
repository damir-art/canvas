# Вставляем изображение
Изображение вставляется как есть, если Canvas меньше изображения, то изображение обрежется.

HTML

    <canvas id="Canvas1" width="700" height="300"></canvas>
    <img id="img1" src="img/bay.jpg" width="715" height="315" style="display:none;" />

JavaScript

    window.onload = function() {
        var theCanvas = document.getElementById('Canvas1')
        if(theCanvas && theCanvas.getContext) {
            var ctx = theCanvas.getContext('2d')
            if(ctx) {
                var srcImg = document.getElementById('img1')
                ctx.drawImage(srcImg, 0, 0)
            }
        }
    }
