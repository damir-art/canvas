# Clipping paths
Создание секущего конутра, обрезка изображений, форм и т.д. внутри Canvas.

    clip()

Изображение обрезано кругом.

    window.onload = function() {
        var theCanvas = document.getElementById('Canvas1')
        if(theCanvas && theCanvas.getContext) {
            var ctx = theCanvas.getContext('2d')
            if(ctx) {
                var srcImg = document.getElementById('img1')

                // Создаём круглый секущий контур
                ctx.arc(ctx.canvas.width / 2, ctx.canvas.height / 2, 150, 0, 2 * Math.PI)
                ctx.clip()

                ctx.drawImage(srcImg, 0, 0)
            }
        }
    }