# Сохраняем состояние
Работаем с функциями save() и restore() сохранить можно следующие свойства strokeStyle, fillStyle, lineWidth и другие.

Помогает писать код быстрее и передавать свойства от объекта к объекту.

    window.onload = function() {
        var theCanvas = document.getElementById('Canvas1')
        if(theCanvas && theCanvas.getContext) {
            var ctx = theCanvas.getContext('2d')
            if(ctx) {
                ctx.strokeStyle = 'red'
                ctx.fillStyle = 'yellow'
                ctx.lineWidth = 10
                ctx.fillRect(25, 25, 100, 125)
                ctx.strokeRect(25, 25, 100, 125)

                ctx.save() // сохранить текущее состояние

                ctx.strokeStyle = 'green'
                ctx.fillStyle = 'blue'
                ctx.lineWidth = 5
                ctx.fillRect(175, 25, 100, 125)
                ctx.strokeRect(175, 25, 100, 125)

                ctx.restore() // загрузить сохранённое состояние

                ctx.fillRect(325, 25, 100, 125)
                ctx.strokeRect(325, 25, 100, 125)
            }
        }
    }