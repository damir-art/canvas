# Заливка обводки
Чтобы залить обводку, нужно вместо `fillRect` использовать `fill`.

    var canvas = document.getElementById('c1')
    var ctx = canvas.getContext('2d')

    ctx.rect(50, 50, 150, 100)

    // Залить обводку
    ctx.fillStyle = '#e74c3c'
    ctx.fill()

    ctx.strokeStyle = '#f1c40f'
    ctx.lineWidth = '20'
    ctx.stroke()

Если `fill` разместить после `stroke` то ширина заливки будет 50%. В нашем примере это 10 пикселей.
