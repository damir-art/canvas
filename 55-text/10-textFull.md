# measureText

`var textW = ctx.measureText(theString)` - добавляем в переменную, текущие настройки текста, в том числе его ширина.

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

                // measureText
                var textW = ctx.measureText(theString)
                // console.log(textW)
                ctx.beginPath()
                ctx.strokeStyle = 'black'
                ctx.moveTo(20, 170)
                ctx.lineTo(textW.width, 170)
                ctx.stroke()
            }
        }
    }