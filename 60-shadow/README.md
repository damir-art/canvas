# Shadow

Создание тени. Тень можно нарисовать на фигуры, линии, пути, текст, изображения и т.д.

Тень может быть окрашена, размыта (blur) и перемещена по x и y.

    shadowColor   - по умолчанию черный
    shadowOffsetX - по умолчанию 0
    shadowOffsetY - по умолчанию 0
    shadowBlur    - по умолчанию 0

Значения тени может быть отрицательным, например (-5) тогда она переместится вверх и влево.

## Прямоугольник, тень

    window.onload = function() {
        var theCanvas = document.getElementById('Canvas1')
        if(theCanvas && theCanvas.getContext) {
            var ctx = theCanvas.getContext('2d')
            if(ctx) {
                // Создаём тень
                ctx.shadowColor = 'rgba(50, 50, 50, 0.5)'
                ctx.shadowOffsetX = 5
                ctx.shadowOffsetY = 5
                ctx.shadowBlur = 10

                // Создаём прямоугольник
                ctx.fillStyle = 'rgba(0, 127, 0, 1)'
                ctx.fillRect(20, 20, 200, 100)
            }
        }
    }