# Линейный градиент

    window.onload = function() {
        var theCanvas = document.getElementById('Canvas1')
        if(theCanvas && theCanvas.getContext) {
            var ctx = theCanvas.getContext('2d')
            if(ctx) {
                /* Линейный градиент */
                // Начальная точка
                var linGrd = ctx.createLinearGradient(20, 20, 20, 280)
                // var linGrd = ctx.createLinearGradient(20, 20, 220, 280)
                // Задаём цвета градиенту
                linGrd.addColorStop(0, '#f00')
                linGrd.addColorStop(0.5, '#00f')
                linGrd.addColorStop(1, '#0f0')
                // Задаём фигуру для градиента
                ctx.fillStyle = linGrd
                ctx.fillRect(20, 20, 200, 260)
                ctx.lineWidth = 3
                ctx.strokeRect(20, 20, 200, 260)
            }
        }
    }