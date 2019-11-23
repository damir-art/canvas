# Обрамление квадрата, заливка квадрата, прозрачный квадрат

Пример очистки, стирания холста:

    window.onload = function() {
        var theCanvas = document.getElementById('Canvas1')
        if(theCanvas && theCanvas.getContext) {
            var ctx = theCanvas.getContext('2d')
            if(ctx) {
                // обрамление квадрата
                ctx.strokeStyle = 'blue'
                ctx.lineWidth = 5
                ctx.strokeRect(25, 25, 100, 125)

                // заливка квадрата
                ctx.fillStyle = 'green'
                ctx.fillRect(175, 25, 100, 125)

                // заливка и обрамление прямоугольника
                ctx.strokeStyle = 'red'
                ctx.fillStyle = 'yellow'
                ctx.lineWidth = 10
                ctx.fillRect(325, 25, 100, 125)
                ctx.strokeRect(325, 25, 100, 125)

                // очистить часть Canvas
                ctx.clearRect(15, 75, 450, 50)
            }
        }
    }