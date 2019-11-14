# Прямоугольник
## Создаём прямоугольник в Canvas

    // Получаем Canvas
    var canvas = document.getElementById('c1')

    // Устанавливаем контекст
    var ctx = canvas.getContext('2d')

    // Создаём прямоугольник
    ctx.fillRect(100, 50, 125, 75)

Прямоугольник начинается с координат x = 100, y = 50, ширина = 125, высота = 75.

По-умолчанию, прямоугольник черного цвета.