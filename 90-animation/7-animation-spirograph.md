# Спирограф
Получаем красивые фигуры. Canvas можно сохранять из браузера как изображение.

    var canvas = document.getElementById('c1')
    var ctx = canvas.getContext('2d')

    var R = 180
    var r = 140
    var d = 50
    var teta = 0
    var timer

    function spiro() {
        var x = (R - r) * Math.cos(teta) + d * Math.cos((R - r) * teta / r)
        var y = (R - r) * Math.sin(teta) - d * Math.sin((R - r) * teta / r)
        teta = teta + 0.1
        ctx.fillRect(x + 300, y + 300, 4, 4)
        timer = setTimeout(spiro, 10)
    }

    spiro()
