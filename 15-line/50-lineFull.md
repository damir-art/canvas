# Нарисовать линии различной ширины

    window.onload = function() {
        var theCanvas = document.getElementById('Canvas1')
        if(theCanvas && theCanvas.getContext) {
            var ctx = theCanvas.getContext('2d')
            if(ctx) {
                for (var i = 0; i < 10; i++) {
                    // Всегда линии в цикле начинаем с beginPath
                    ctx.beginPath()
                    ctx.lineWidth = i + 1
                    ctx.moveTo(25, 25 + i * 15)
                    ctx.lineTo(475, 25 + i * 15)
                    // Всегда линии заканчиваем со stroke
                    ctx.stroke()
                }
            }
        }
    }
