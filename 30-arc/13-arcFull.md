# Градусы, радианы
Как делать градусы вместо радиан. Создаём окружность в 160 градусов.

    // 360 градусов, круг, обрамлен и заполнен
    var degress = 160
    var radians = Math.PI / 180 * degress
    ctx.beginPath()
    ctx.arc(550, 150, 100, 0, radians)
    ctx.fill()
    ctx.stroke()

