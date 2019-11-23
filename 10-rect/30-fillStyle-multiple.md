# Несколько прямоугольников
## Создаём несколько прямоугольников в Canvas

    var canvas = document.getElementById('c1')
    var ctx = canvas.getContext('2d')

    // Emerald
    ctx.fillStyle = '#2ecc71'
    ctx.fillRect(25, 25, 100, 50)

    // Sun flower
    ctx.fillStyle = '#f1c40f'
    ctx.fillRect(125, 100, 125, 75)

    // Alizarin
    ctx.fillStyle = '#e74c3c'
    ctx.fillRect(300, 25, 75, 75)
