# Paint
## Рисуем в Canvas

    var canvas = document.getElementById('c1')
    var ctx = canvas.getContext('2d')

    // При нажатии на мышь
    canvas.onmousedown = function(event) {
        // Отслеживаем движение мышью
        canvas.onmousemove = function(event) {
            // Определяем координаты мыши
            var x = event.offsetX
            var y = event.offsetY
            // Закрашиваем участок
            ctx.fillRect(x-5, y-5, 10, 10)
            // console.log(x, y)
        }
        // При отжатии кнопки мыши, прекращаем рисовать
        canvas.onmouseup = function(event) {
            canvas.onmousemove = null
        }
        // console.log(x, y)
    }
