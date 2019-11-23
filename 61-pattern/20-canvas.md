# Паттерн "Канвас"
Паттерн из Canvas.

HTML

    <canvas id="Canvas1" width="700" height="300"></canvas>
    <canvas id="patCan"  width="25"  height="25"></canvas>

JavaScript

    window.onload = function() {
        var theCanvas = document.getElementById('Canvas1')
        if(theCanvas && theCanvas.getContext) {
            var ctx = theCanvas.getContext('2d')
            if(ctx) {
                var patCanvas = document.getElementById('patCan')
                var patCtx = patCanvas.getContext('2d')
                patCtx.strokeStyle = 'red'
                patCtx.lineWidth = 1
                patCtx.beginPath()
                patCtx.moveTo(0, 0)
                patCtx.lineTo(25, 25)
                patCtx.stroke()

                var strokePat = ctx.createPattern(patCanvas, 'repeat')
                ctx.strokeStyle = strokePat
                ctx.lineWidth = 25
                ctx.strokeRect(50, 50, 200, 200)
            }
        }
    }