# Линия
## Рисуем линию в Canvas
Функции для работы с линиями:

    moveTo(x, y) - рисуем линию, начальная координата
    lineTo(x, y) - рисуем линию, конечная координата
    lineWidth    - ширина линии 
    lineCap      - концы линии butt, round, square
    lineJoin     - как линия соединяется по кругу (round), под наклоном (bevel), под скосом (miter, по-умолчанию)
    miterLimit
    beginPath    - начало рисования линии
    stroke()     - нарисовать

### Задаём начальное и конечное положения пера

    var canvas = document.getElementById('c1')
    var ctx = canvas.getContext('2d')

    // Начальные координаты пера (x, y)
    ctx.moveTo(50, 50)

    // Конечные координаты пера (x, y)
    ctx.lineTo(150, 150)

    // Создать линию
    ctx.stroke()

### Добавляем цвет и ширину линии

    ctx.moveTo(50, 50)
    ctx.lineTo(150, 150)

    // Цвет линии
    ctx.strokeStyle = 'green'

    // Ширина линии
    ctx.lineWidth = '5'

    ctx.stroke()

### Добавляем линию

    /* Создание линии */
    ctx.moveTo(50, 50)
    ctx.lineTo(100, 150)
    ctx.lineWidth = '5'
    ctx.strokeStyle = 'green'

    // Добавляем линию
    ctx.lineTo(200, 50)

    ctx.stroke()
