# Несколько линий
## Создаём несколько разных линий `ctx.beginPath()`

    var canvas = document.getElementById('c1')
    var ctx = canvas.getContext('2d')

    /* Первая линия */
    ctx.beginPath()
    ctx.moveTo(50, 50)
    ctx.lineTo(100, 150)
    ctx.lineWidth = '20'
    ctx.strokeStyle = '#f1c40f'
    ctx.stroke()

    /* Вторая линия */
    ctx.beginPath()
    ctx.moveTo(150, 50)
    ctx.lineTo(200, 150)
    ctx.lineWidth = '20'
    ctx.strokeStyle = '#2ecc71'
    ctx.stroke()
