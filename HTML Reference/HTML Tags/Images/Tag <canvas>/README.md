# Тег canvas

Тег ``<canvas>`` представляет возможность рисования графики на веб-страницах с использованием JavaScript. Тег ``<canvas>`` представляет собой контейнер, который можно использовать для рисования графики на веб-странице. Он предоставляет JavaScript API для рисования различных форм, линий, текста и изображений.
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tag canvas</title>
</head>
<body>
    <canvas id="canvasDemo" width="500" height="500"></canvas>

    <script>
        const canvas = document.getElementById("canvasDemo");
        const context = canvas.getContext("2d");

        // Прямоугольник
        context.fillStyle="blue";
        context.fillRect(20, 20, 100, 100);

        // Круг
        context.fillStyle="green";
        const circle = new Path2D();
        circle.arc(100, 100, 50, 0, 2 * Math.PI);

        context.fill(circle);

        // Линия
        context.beginPath();
        context.moveTo(100, 150);
        context.lineTo(200, 150);
        context.stroke();

        // Текст
        context.font = "20px Arial";
        context.fillText("Привет, Canvas", 20, 20);
    </script>
</body>
</html>
```

Тег ``<canvas>`` используется для рисования графики на лету с помощью сценариев (обычно JavaScript). Тег ``<canvas>`` является прозрачным и это всего лишь контейнер для графики, для ее рисования необходимо использовать скрипт.

Любой текст внутри элемента ``<canvas>`` будет отображаться в браузерах с отключенным JavaScript и в браузерах, не поддерживающих ``<canvas>``.

## Атрибуты

- **height:** pixels | Указывает высоту холста. Значение по умолчанию - 150.
- **width:** pixels | Указывает ширину холста. Значение по умолчанию - 300.

## Примечания

- Тег ``<canvas>`` поддерживает глобальные атрибуты в HTML.
- Тег ``<canvas>`` поддерживает атрибуты событий в HTML.

## Настройки CSS по умолчанию

Большинство браузеров отображают элемент ``<canvas>`` со следующими значениями по умолчанию:

```
canvas {
    height: 150px;
    width: 300px;
}
```

## Заключение

Тег ``<canvas>`` в HTML предоставляет мощный инструмент для создания графических элементов на веб-страницах. Совместно с JavaScript он позволяет реализовывать разнообразные визуальные эффекты и интерактивные элементы.