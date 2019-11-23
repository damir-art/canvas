# Прямоугольник, текст, тень

    window.onload = function() {
        var theCanvas = document.getElementById('Canvas1')
        if(theCanvas && theCanvas.getContext) {
            var ctx = theCanvas.getContext('2d')
            if(ctx) {
                // Создаём тень
                ctx.shadowColor = 'rgba(50, 50, 50, 0.5)'
                ctx.shadowOffsetX = 5
                ctx.shadowOffsetY = 5
                ctx.shadowBlur = 7

                // Создаём прямоугольник
                ctx.fillStyle = 'rgba(0, 127, 0, 1)'
                ctx.fillRect(20, 20, 200, 100)

                // Создаём текст
                var theString = 'Drawing Text on a Canvas'
                ctx.fillStyle = 'rgba(0, 127, 0, 1)'
                ctx.shadowColor = 'rgba(0, 127, 0, 0.5)'
                ctx.shadowOffsetX = 3
                ctx.shadowOffsetY = 3
                ctx.shadowBlur = 3
                ctx.font = '25pt Georgia'
                ctx.fillText(theString, 250, 75)
            }
        }
    }