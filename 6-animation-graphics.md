# Анимация графика
Анимируем график синуса или косинуса.

    var canvas = document.getElementById('c1')
    var ctx = canvas.getContext('2d')

    var x = 0
    var y
    var timer

    function drawSin() {
        y = Math.sin(x)
        x = x + 0.3
        ctx.fillRect(x * 4, y * 20 + 100, 2, 2)
        timer = setTimeout(drawSin, 100)
    }

    drawSin()
