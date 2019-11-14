# Шаблон Canvas
Начальный шаблон для работы с Canvas. Расположение папок и файлов в проекте.

* Сетка: файл jpg|png|gif, с размерами 1280x720, с координатами x, y.
* HTML-файл с тегом Canvas.
* CSS-файл с правилами для Canvas и сетки.
* JavaScript-файл для задания Canvas и контекста.

## Структура проекта

    img/
        grid-canvas.png
    index.html
    style.css
    canvas.js

## Что располагается внутри файлов?
### HTML (index.html)
Ширина и высота это пропорции:

    <canvas id="c1" width="400" height="200"></canvas>

### CSS (style.css)
Задаём те размеры которые хотим увидеть на HTML-странице.

    body {
	    margin: 0;
    }
    #c1 {
        width: 400px;
        height: 200px;
        border: 3px solid black;
        margin: 20px;
        background-image: url(img/grid-canvas.png);
    }

### JavaScript (canvas.js)
Создаём переменные для Canvas и контекста:

    // Получаем canvas
    var canvas = document.getElementById('c1')

    // Устанавливаем контекст
    var ctx = canvas.getContext('2d')

## Разное
* Координаты в Canvas, начинаются с левого верхнего угла.
* Можно задавать отрицательные координаты.
* Разрешение Canvas, может не совпадать с его физическими размерами в HTML.
