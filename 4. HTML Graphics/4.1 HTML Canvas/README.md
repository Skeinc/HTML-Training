# HTML Canvas

HTML Canvas - это мощный инструмент, позволяющий веб-разработчикам воплощать свои творческие идеи в интерактивных графических элементах прямо на веб-страницах. Этот элемент HTML открывает двери для создания анимаций, игр, графиков и многого другого. Давайте глубже погрузимся в мир HTML Canvas и его возможности.

Элемент HTML ``<canvas>`` используется для рисования графики на веб-странице.

## Что такое HTML-холст?

Элемент HTML ``<canvas>`` используется для рисования графики на лету с помощью JavaScript.

Элемент ``<canvas>`` представляет собой всего лишь контейнер для графики. Вы должны использовать JavaScript для рисования графики.

В ``<canvas>`` имеется несколько методов рисования контуров, прямоугольников, кругов, текста и добавления изображений.

Canvas поддерживается всеми основными браузерами.

## Примеры холстов

Холст - это прямоугольная область на HTML-странице. По умолчанию холст не имеет границ и содержимого.

Разметка выглядит следующим образом:

```
<canvas id="exampleCanvas" width="200" height="100" style="border: 1px solid #000;"></canvas>
```

**Примечание:** Всегда указывайте ``id`` атрибут (который будет указан в сценарии), а также атрибут ``width`` и ``height`` для определения размера холста. Чтобы добавить границу, используйте ``style`` атрибут.

## Добавить JavaScript

После создания прямоугольной области холста вам необходимо добавить JavaScript для рисования.

Вот некоторые примеры:

```
<canvas id="strokeCanvas" width="200" height="100" style="border: 1px solid #000;"></canvas>
<script>
    var c = document.getElementById("strokeCanvas");
    var ctx = c.getContext("2d");

    ctx.moveTo(0, 0);
    ctx.lineTo(200, 100);
    ctx.stroke();
</script>
```

### Нарисовать круг

```
<canvas id="circleCanvas" width="200" height="100" style="border: 1px solid #000;"></canvas>
<script>
    var c = document.getElementById("circleCanvas");
    var ctx = c.getContext("2d");

    ctx.beginPath();
    ctx.arc(95, 50, 40, 0, 2 * Math.PI);
    ctx.stroke();
</script>
```

### Нарисовать текст

```
<canvas id="textCanvas" width="200" height="100" style="border: 1px solid #000;"></canvas>
<script>
    var c = document.getElementById("textCanvas");
    var ctx = c.getContext("2d");

    ctx.font = "30px Arial";
    ctx.fillText("Hello, World", 10, 50);
</script>
```

### Обводка текста

```
<canvas id="strokeCanvas" width="200" height="100" style="border: 1px solid #000;"></canvas>
<script>
    var c = document.getElementById("textCanvas");
    var ctx = c.getContext("2d");

    ctx.font = "30px Arial";
    ctx.strokeText("Hello, World", 10, 50);
</script>
```

### Нарисовать линейный градиент

```
<canvas id="linearGradientCanvas" width="200" height="100" style="border: 1px solid #000;"></canvas>
<script>
    var c = document.getElementById("linearGradientCanvas");
    var ctx = c.getContext("2d");

    var grd = ctx.createLinearGradient(0, 0, 200, 0);
    grd.addColorStop(0, "red");
    grd.addColorStop(1, "white");

    ctx.fillStyle = grd;
    ctx.fillRect(10, 10, 150, 80);
</script>
```

### Нарисуйте круговой градиент

```
<canvas id="circularGradientCanvas" width="200" height="100" style="border: 1px solid #000;"></canvas>
<script>
    var c = document.getElementById("circularGradientCanvas");
    var ctx = c.getContext("2d");

    var grd = ctx.createRadialGradient(75, 50, 5, 90, 60, 100);
    grd.addColorStop(0, "red");
    grd.addColorStop(1, "white");

    ctx.fillStyle = grd;
    ctx.fillRect(10, 10, 150, 80);
</script>
```

## Заключение

HTML Canvas предоставляет веб-разработчикам увлекательный инструмент для создания динамичных и интерактивных графических элементов. С его помощью вы можете реализовывать свои творческие идеи, добавлять визуальное волшебство на ваши веб-страницы и обеспечивать пользователям захватывающий опыт взаимодействия.