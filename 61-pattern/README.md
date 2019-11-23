# Паттерн
Патерны можно создавать из изображения, gif (первый кадр), видео (первый кадр) или фигуры Canvas.

    createPattern(elem, repeat)

    elem   - изображение, видео и т.д.
    repeat - no-repeat, repeat, repeat-x, repeat-y

Не работает, выяснить почему:

    window.onload = function() {
        var theCanvas = document.getElementById('Canvas1')
        if(theCanvas && theCanvas.getContext) {
            var ctx = theCanvas.getContext('2d')
            if(ctx) {
                var patImg = new Image()
                patImg.onload = function() {
                    ctx.fillStyle = ctx.createPattern(patImg, 'repeat')
                    ctx.fillRect(0, 0, ctx.canvas.width, ctx.canvas.height)
                }
                patImg.src = 'img/pic.gif'
            }
        }
    }