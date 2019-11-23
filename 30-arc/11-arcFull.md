# Дуги
Дуги это кривые, которые являются частями окружности. Окружность это тоже дуга.

Чтобы нарисовать дугу, нужно использовать функцию arc() или arcTo()

* `arc(x, y, r, sA, eA, aC)`
* `arcTo(x1, y1, x2, y2, r)`
* `closePath()` - закрывает текущий контур

x, y - центр круга, если дуга полная окружность<br />
r - радиус<br />
sA, eA - начальный и конечный угол, при создании дуги<br />
true/false - против часовой, по часовой

x1, y1, x2, y2, r - две точки и радиус

Углы рассчитываются в радианах. С использованием математических функций `радиан = Math.Pi / 180 * градус` можно пользоваться градусами вместо радиан.

    360 градусов = 2 Pi радиан

    window.onload = function() {
        var theCanvas = document.getElementById('Canvas1')
        if(theCanvas && theCanvas.getContext) {
            var ctx = theCanvas.getContext('2d')
            if(ctx) {
                // 90 градусов, по часовой стрелке
                ctx.beginPath()
                ctx.arc(50, 150, 100, 1.5 * Math.PI, 2 * Math.PI)
                ctx.stroke()
            }
        }
    }

Идем от нулевой части угла (90 градусов) до 1.5 (180 градусов) радиан против часовой стрелки.

    window.onload = function() {
        var theCanvas = document.getElementById('Canvas1')
        if(theCanvas && theCanvas.getContext) {
            var ctx = theCanvas.getContext('2d')
            if(ctx) {
                ctx.strokeStyle = 'blue'
                ctx.fillStyle = 'red'
                ctx.lineWidth = '5'
                
                ctx.beginPath()
                ctx.arc(50, 150, 100, 1.5 * Math.PI, 2 * Math.PI)
                ctx.stroke()

                // 270 градусов, против часовой стрелки
                ctx.beginPath()
                ctx.arc(300, 150, 100, 0, 1.5 * Math.PI, false)
                ctx.stroke()
            }
        }
    }