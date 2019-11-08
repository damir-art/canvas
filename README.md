# Canvas
Изучаем Canvas для создания игр на HTML5 и JavaScript

## Начинаем работать с Canvas
* Создаем сетку 1280x720

### HTML
Ширина и высота это пропорции?

    <canvas id="c1" width="400" height="200"></canvas>

### CSS
Задаём те размеры которые хотим увидеть на HTML-странице.

    #c1 {
        width: 400px;
        height: 200px;
        border: 3px solid black;
        margin: 40px;
        background-image: url(setka.png);
    }

### JavaScript
    // Получаем canvas
    var canvas = document.getElementById('c1')

    // Устанавливаем контекст
    var ctx = canvas.getContext('2d')

    // Создаём прямоугольник
    ctx.fillRect(100, 50, 75, 25);

Прямоугольник по-умолчанию черный. 100 = x, 50 = y, 75 = ширина, 25 = высота 

## Разное
* Координаты в Canvas, начинаются с левого верхнего угла.
* Можно задавать отрицательные координаты.
