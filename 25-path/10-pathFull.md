# beginPath
Контур из трех сегментов, не закрытый.

    window.onload = function() {
        var theCanvas = document.getElementById('Canvas1')
        if(theCanvas && theCanvas.getContext) {
            var ctx = theCanvas.getContext('2d')
            if(ctx) {
                // Не закрытый контур
                ctx.strokeStyle = 'blue'
                ctx.fillStyle = 'red'
                ctx.lineWidth = 5

                ctx.beginPath()
                ctx.moveTo(25, 175)
                ctx.lineTo(50, 25)
                ctx.lineTo(125, 50)
                ctx.lineTo(175, 175)
                ctx.stroke()
            }
        }
    }