# Кривые безье
Есть начальная точка, есть конечная точка, есть еще две контрольные точки отвечающие за кривую.

Кривые безье немного сложнее квадратичных кривых.

    bezierCurveTo(cx1, cy1, cx2, cy2, end1, end2)

    cx1, cy1, cx2, cy2 - контрольные точки

    window.onload = function() {
        var theCanvas = document.getElementById('Canvas1')
        if(theCanvas && theCanvas.getContext) {
            var ctx = theCanvas.getContext('2d')
            if(ctx) {
                // Создаем крувую безье
                ctx.strokeStyle = 'blue'
                ctx.lineWidth = '5'
            
                ctx.beginPath()
                ctx.moveTo(50, 200)
                ctx.bezierCurveTo(50, 100, 200, 100, 200, 150)
                ctx.stroke()

                // Делаем контрольные точки видимыми
                ctx.strokeStyle = 'rgba(0, 0, 0, .25)'
                ctx.lineWidth = 1

                ctx.beginPath()
                ctx.moveTo(50, 200)
                ctx.lineTo(50, 100)
                ctx.lineTo(200, 100)
                ctx.lineTo(200, 150)
                ctx.stroke()
            }
        }
    }