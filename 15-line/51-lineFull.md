# strokeStyle, lineCap
Смотри как выглядят концы линий.

    window.onload = function() {
        var theCanvas = document.getElementById('Canvas1')
        if(theCanvas && theCanvas.getContext) {
            var ctx = theCanvas.getContext('2d')
            if(ctx) {
                // 1
                ctx.beginPath()
                ctx.strokeStyle = 'cyan'
                ctx.lineWidth = 1
                ctx.moveTo(50, 25)
                ctx.lineTo(50, 175)
                ctx.moveTo(450, 25)
                ctx.lineTo(450, 175)
                ctx.stroke()

                // 2
                ctx.lineWidth = 25
                ctx.strokeStyle = 'black'
                ctx.lineCap = 'butt'
                ctx.beginPath()
                ctx.moveTo(50, 50)
                ctx.lineTo(450, 50)
                ctx.stroke()

                ctx.lineCap = 'round'
                ctx.beginPath()
                ctx.moveTo(50, 100)
                ctx.lineTo(450, 100)
                ctx.stroke()

                ctx.lineCap = 'square'
                ctx.beginPath()
                ctx.moveTo(50, 150)
                ctx.lineTo(450, 150)
                ctx.stroke()
            }
        }
    }