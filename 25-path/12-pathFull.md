# fill()
Контур из трех сегментов, залитый.

    window.onload = function() {
        var theCanvas = document.getElementById('Canvas1')
        if(theCanvas && theCanvas.getContext) {
            var ctx = theCanvas.getContext('2d')
            if(ctx) {
                ctx.strokeStyle = 'blue'
                ctx.fillStyle = 'red'
                ctx.lineWidth = 5

                // Не закрытый контур
                ctx.beginPath()
                ctx.moveTo(25, 175)
                ctx.lineTo(50, 25)
                ctx.lineTo(125, 50)
                ctx.lineTo(175, 175)
                ctx.stroke()

                // Закрытый контур
                ctx.beginPath()
                ctx.moveTo(225, 175)
                ctx.lineTo(250, 25)
                ctx.lineTo(325, 50)
                ctx.lineTo(375, 175)
                ctx.closePath()
                ctx.stroke()

                // Закрытый контур, залитый
                ctx.beginPath()
                ctx.moveTo(425, 175)
                ctx.lineTo(450, 25)
                ctx.lineTo(525, 50)
                ctx.lineTo(575, 175)
                // ctx.closePath()
                ctx.fill()
                ctx.stroke()
            }
        }
    }