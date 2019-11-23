# Квадратичные кривые
Есть начальная точка, есть конечная точка, есть еще одна контрольная точка отвечающая за кривую.

Квадратичные кривые немного легче кривых безье.

    quadraticCurveTo(cx, cy, x, y)

    window.onload = function() {
        var theCanvas = document.getElementById('Canvas1')
        if(theCanvas && theCanvas.getContext) {
            var ctx = theCanvas.getContext('2d')
            if(ctx) {
                // Создаем кривую безье
                ctx.strokeStyle = 'green'
                ctx.lineWidth = '5'
            
                ctx.beginPath()
                ctx.moveTo(400, 200)
                ctx.quadraticCurveTo(400, 100, 600, 150)
                ctx.stroke()

                // Делаем контрольные точки видимыми
                ctx.strokeStyle = 'rgba(0, 0, 0, .25)'
                ctx.lineWidth = 1

                ctx.beginPath()
                ctx.moveTo(400, 200)
                ctx.lineTo(400, 100)
                ctx.lineTo(600, 150)
                ctx.stroke()
            }
        }
    }