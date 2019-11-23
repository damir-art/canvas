# 360 градусов, круг
360 градусов, круг, обрамлен и заполнен

    window.onload = function() {
        var theCanvas = document.getElementById('Canvas1')
        if(theCanvas && theCanvas.getContext) {
            var ctx = theCanvas.getContext('2d')
            if(ctx) {
                ctx.strokeStyle = 'blue'
                ctx.fillStyle = 'red'
                ctx.lineWidth = '5'
                
                ctx.beginPath()
                ctx.arc(50, 150, 100, 1.5 * Math.PI, 2 * Math.PI)
                ctx.stroke()

                // 270 градусов, против часовой стрелки
                ctx.beginPath()
                ctx.arc(300, 150, 100, 0, 1.5 * Math.PI, false)
                ctx.stroke()

                // 360 градусов, круг, обрамлен и заполнен
                ctx.beginPath()
                ctx.arc(550, 150, 100, 0, 2 * Math.PI)
                ctx.fill()
                ctx.stroke()
            }
        }
    }