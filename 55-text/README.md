# Текст
Создание текстов в Canvas

    font (family, size, weight, variant и т.п)
    textAlign (start, end, left, right, center)
    textBaseline (top, hanging, middle, alphabetic, ideographic, bottom)
    fillText(txt, x, y, [maxW])
    strokeText(txt, x, y, [maxW])
    measureText(text)

Рисуем текст по координатам, размеру шрифта, цвету, обводкой.

    window.onload = function() {
        var theCanvas = document.getElementById('Canvas1')
        if(theCanvas && theCanvas.getContext) {
            var ctx = theCanvas.getContext('2d')
            if(ctx) {
                // Текст по умолчанию
                var theString = 'Drawing Text on a Canvas!'
                ctx.fillText(theString, 20, 20)
                
                // Текст со шрифтом
                ctx.font = '25pt Georgia'
                ctx.fillText(theString, 20, 60)

                // Текст с цветом
                ctx.fillStyle = 'blue'
                ctx.fillText(theString, 20, 100)

                // Текст с обрамлением
                ctx.font = '32pt Verdana'
                // ctx.textBaseline = 'middle'
                ctx.fillStyle = 'yellow'
                ctx.strokeStyle = 'rgba(0, 255, 0, 0.8)'
                ctx.fillText(theString, 20, 160)
                ctx.strokeText(theString, 20, 160)
           }
        }
    }