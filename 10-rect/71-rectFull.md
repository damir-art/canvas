# Обрамление квадрата, заливка квадрата:

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
            }
        }
    }
