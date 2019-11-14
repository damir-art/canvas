# Цвет прямоугольника
## Создаём прямоугольник в Canvas

    var canvas = document.getElementById('c1')
    var ctx = canvas.getContext('2d')

    // Заливаем прямоугольник цветом
    ctx.fillStyle = 'green'

    ctx.fillRect(100, 50, 125, 75)

Вместо `green` можно использовать `#0000ff`
