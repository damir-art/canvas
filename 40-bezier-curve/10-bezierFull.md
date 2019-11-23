window.onload = function() {
    var theCanvas = document.getElementById('Canvas1')
    if(theCanvas && theCanvas.getContext) {
        var ctx = theCanvas.getContext('2d')
        if(ctx) {
            // Создаем кривую безье
            ctx.strokeStyle = 'blue'
            ctx.lineWidth = '5'
        
            ctx.beginPath()
            ctx.moveTo(50, 200)
            ctx.bezierCurveTo(50, 300, 200, 100, 200, 150)
            ctx.stroke()

            // Делаем контрольные точки видимыми
            ctx.strokeStyle = 'rgba(0, 0, 0, .25)'
            ctx.lineWidth = 1

            ctx.beginPath()
            ctx.moveTo(50, 200)
            ctx.lineTo(50, 300)
            ctx.lineTo(200, 100)
            ctx.lineTo(200, 150)
            ctx.stroke()
        }
    }
}