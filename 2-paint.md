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

Добавляем возможность рисовать разными красками, цвет назначаем через `input` в HTML:

HTML:

    <div><input type="color" id="color" /></div>
    <canvas id="c1" width="400" height="200"></canvas>

JavaScript:

    var canvas = document.getElementById('c1')
    var ctx = canvas.getContext('2d')
    var myColor = 'green'

    document.getElementById('color').oninput = function(event) {
        myColor = this.value
        console.log(myColor)
    }

    canvas.onmousedown = function(event) {
        canvas.onmousemove = function(event) {
            var x = event.offsetX
            var y = event.offsetY
            ctx.fillRect(x-5, y-5, 10, 10)
            ctx.fillStyle = myColor
            ctx.fill()
        }
        canvas.onmouseup = function(event) {
            canvas.onmousemove = null
        }
    }

## Кисточка без углов и прерываний

    var canvas = document.getElementById('c1')
    var ctx = canvas.getContext('2d')
    var myColor = 'green'

    document.getElementById('color').oninput = function(event) {
        myColor = this.value
        ctx.beginPath()
    }

    canvas.onmousedown = function(event){
        var x = event.offsetX;
        var y = event.offsetY;
        ctx.strokeStyle = myColor
        ctx.lineCap = 'round'
        ctx.lineWidth = 5
        ctx.moveTo (x, y);
        canvas.onmousemove = function (event){
            var x = event.offsetX;
            var y = event.offsetY;
            ctx.lineTo (x, y)
            ctx.stroke()
        }
        canvas.onmouseup = function(){
            canvas.onmousemove = null;
        }
    }
