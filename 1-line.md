# Линия
## Рисуем линию в Canvas

Задаём начальное и конечное положения пера.

    var canvas = document.getElementById('c1')
    var ctx = canvas.getContext('2d')

    /* Создание линии */
    // Начальные координаты пера (ширина, высота)
    ctx.moveTo(100, 50)
    // Конечные координаты пера
    ctx.lineTo(150, 150)
    // Цвет линии
    ctx.strokeStyle = 'green'
    // Ширина линии
    ctx.lineWidth = '5'
    // Создать линию
    ctx.stroke()

Продолжаем линию:

    /* Добавление линии */
    ctx.lineTo(200, 50)
    ctx.stroke()

Создаём несколько разных линий `ctx.beginPath()`:

    /* Создание новой линии */
    ctx.beginPath()
    ctx.moveTo(100, 50)
    ctx.lineTo(150, 150)
    ctx.strokeStyle = 'green'
    ctx.lineWidth = '5'
    ctx.stroke()

    ctx.beginPath()
    ctx.strokeStyle = 'orange'
    ctx.lineWidth = '10'
    ctx.moveTo(150, 50)
    ctx.lineTo(200, 50)
    ctx.stroke()
