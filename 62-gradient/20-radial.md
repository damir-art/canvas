# Радиальный градиент

    window.onload = function() {
        var theCanvas = document.getElementById('Canvas1')
        if(theCanvas && theCanvas.getContext) {
            var ctx = theCanvas.getContext('2d')
            if(ctx) {
                /* Радиальный градиент */
                // var radGrd = ctx.createRadialGradient(525, 150, 20, 525, 150, 100)
                var radGrd = ctx.createRadialGradient(500, 100, 20, 525, 150, 100)
                // Задаём цвета градиенту
                radGrd.addColorStop(0, '#f00')
                radGrd.addColorStop(0.5, '#00f')
                radGrd.addColorStop(1, '#0f0')
                ctx.fillStyle = radGrd

                ctx.beginPath()
                ctx.arc(525, 150, 100, 0, 2 * Math.PI)
                ctx.stroke()
                ctx.fill()
            }
        }
    }