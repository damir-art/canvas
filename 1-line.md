# Линия
## Рисуем линию в Canvas

Задаём начальное положение пера и конечное.

    var canvas = document.getElementById('c1')
    var ctx = canvas.getContext('2d')

    // Начальные координаты пера
    ctx.moveTo(100, 50)
    // Конечные координаты пера
    ctx.lineTo(150, 150)
    // Цвет линии
    ctx.strokeStyle = 'green'
    // Ширина линии
    ctx.lineWidth = '5'
    // Линия
    ctx.stroke()
