# Обводка
Чтобы создать обводку, нужно вместо `fillRect` использовать `rect`.

    var canvas = document.getElementById('c1')
    var ctx = canvas.getContext('2d')

    // Координаты обводки
    ctx.rect(50, 50, 150, 100)

    // Цвет обводки
    ctx.strokeStyle = '#f1c40f'

    // Ширина обводки
    ctx.lineWidth = '20'

    // Создать обводку
    ctx.stroke()
