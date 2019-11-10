# Круг
Создаём дуги и окружности в Canvas.

Порядок создания круга:
* Задаём центр окружности
* Радиус окружности
* `true` против часовой, `false` по часовой
* pi == 180 градусов

Пример окружности:

    var canvas = document.getElementById('c1')
    var ctx = canvas.getContext('2d')
    var pi = Math.PI

    // Толщина обводки
    ctx.lineWidth = 5

    // Цвет обводки
    ctx.strokeStyle = 'green'

    // Цвет заливки
    ctx.fillStyle = 'orange'

    // Центр окружности, радиус, угол окружности
    ctx.arc(100, 100, 50, 0, pi*2, false)

    // Выполнить обводку
    ctx.stroke()

    // Выполнить заливку
    ctx.fill()

## PS
* Используем `ctx.beginPath()` и `ctx.closePath()`, если окружностей несколько.
* `ctx.arc(100, 100, 50, 0, pi*2, false)` полную окружность нужно делать через `false`
