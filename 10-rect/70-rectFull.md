# Порядок выполнения команд
Рассмотрим скрипт с использованием всех команд.

## Создаём зелёный прямоугольник

    window.onload = function() {
        var theCanvas = document.getElementById('Canvas1')
        if(theCanvas && theCanvas.getContext) {
            var ctx = theCanvas.getContext('2d')
            if(ctx) {
                ctx.fillStyle = 'green'
                ctx.fillRect(20, 20, 100, 100)
            }
        }
    }

## Создаём зелёный прямоугольник с обводкой

    window.onload = function() {
        var theCanvas = document.getElementById('Canvas1')
        if(theCanvas && theCanvas.getContext) {
            var ctx = theCanvas.getContext('2d')
            if(ctx) {
                ctx.fillStyle = 'green'
                ctx.fillRect(20, 20, 100, 100)

                ctx.lineWidth = 5
                ctx.strokeStyle = 'rgba(255, 150, 50, 1)'
                ctx.strokeRect(20, 20, 100, 100)
            }
        }
    }