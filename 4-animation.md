# Анимация
Анимация радиуса круга. Радиус круга движется за мышкой.

    var canvas = document.getElementById('c1')
    var ctx = canvas.getContext('2d')
    var pi = Math.PI

    canvas.onmousemove = function(event) {
        var x = event.offsetX
        ctx.clearRect(0, 0, 400, 200)

        ctx.beginPath()
        ctx.lineWidth = 5
        ctx.strokeStyle = 'green'
        ctx.fillStyle = 'orange'
        ctx.arc(200, 100, Math.abs(x-200), 0, pi*2, false)
        ctx.stroke()
        ctx.fill()
    }
