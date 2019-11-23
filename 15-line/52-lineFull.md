# lineJoin
Форма соединения отрезков

    window.onload = function() {
        var theCanvas = document.getElementById('Canvas1')
        if(theCanvas && theCanvas.getContext) {
            var ctx = theCanvas.getContext('2d')
            if(ctx) {
                ctx.lineWidth = 15
                ctx.strokeStyle = 'black'
                ctx.lineJoin = 'round'
                ctx.beginPath()
                ctx.moveTo(25, 150)
                ctx.lineTo(75, 50)
                ctx.lineTo(125, 150)
                ctx.stroke()

                ctx.lineJoin = 'bevel'
                ctx.beginPath()
                ctx.moveTo(175, 150)
                ctx.lineTo(225, 50)
                ctx.lineTo(275, 150)
                ctx.stroke()

                ctx.lineJoin = 'miter' // по умолчанию 10
                // ctx.miterLimit = 1
                ctx.beginPath()
                ctx.moveTo(325, 150)
                ctx.lineTo(375, 50)
                ctx.lineTo(425, 150)
                ctx.stroke()
            }
        }
    }