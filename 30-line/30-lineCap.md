# Концы линий
Создаём концы для линий.

    butt (по-умолчанию)
    round (круглые)
    square (квадратные)

Пример:

    /* Первая линия */
    ctx.beginPath()
    ctx.moveTo(50, 50)
    ctx.lineTo(100, 150)
    ctx.lineWidth = '20'
    ctx.strokeStyle = '#f1c40f'
    ctx.lineCap = 'round' // круглые концы
    ctx.stroke()

    /* Вторая линия */
    ctx.beginPath()
    ctx.moveTo(150, 50)
    ctx.lineTo(200, 150)
    ctx.lineWidth = '20'
    ctx.strokeStyle = '#2ecc71'
    ctx.lineCap = 'square' // квадратные концы
    ctx.stroke()

Для каждой линии нужно задавать свой `lineCap`, если хотите чтобы у каждой линии он был разный.