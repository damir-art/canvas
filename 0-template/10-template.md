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

    <canvas id="c1" width="400" height="200"></canvas>

### CSS (style.css)

    body {
	    margin: 0;
    }
    #c1 {
        // width: 400px;
        // height: 200px;
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

## API 2D
API 2D состоит из функций трёх видов.

### Работы с формами (что рисуется)
* Прямоугольники
* Линии, фигуры
* Дуги, окрухности
* Контуры
* Цвета, стили
* Текст
* Кривые безье
* Квадратичные кривые

### Как рисуется
* Композиция
* Паттерны, узоры
* Градиенты
* Тени
* Обрезка путей

### Медиа
* Изображения
* Трансформации
* Видео
* Raw пиксели

## Разное
Высоту и ширину можно прописать через JavaScript:

    window.onload = function() {
        var canvas = document.getElementById('Canvas1')
        canvas.width = 150
        canvas.height = 150
    }

Продвинутый шаблон для JavaScript, серый фон:

    window.onload = function() {
        var theCanvas = document.getElementById('Canvas1')
        if(theCanvas && theCanvas.getContext) {
            var ctx = theCanvas.getContext('2d')
            if(ctx) {
                ctx.fillStyle = 'lightGray'
                ctx.fillRect(0, 0, ctx.canvas.width, ctx.canvas.height)
            }
        }
    }

* Координаты в Canvas, начинаются с левого верхнего угла.
* Можно задавать отрицательные координаты.
* Разрешение Canvas, может не совпадать с его физическими размерами в HTML.
* При рисовании в Canvas, например фигур, сначала определяют свойства, потом методы.
* Фигуры внутри Canvas это не объекты DOM, это просто нарисованные пиксели.
* Анимация, события, реакция происходит за счет полного обновления холста и не части изображения (фигуры).