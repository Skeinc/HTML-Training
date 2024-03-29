# HTML SVG

Scalable Vector Graphics (SVG) в HTML предоставляет возможность создавать графические элементы, которые легко масштабируются без потери качества. SVG - это мощный инструмент для веб-разработчиков, открывающий широкие возможности для создания векторных изображений, анимаций и интерактивных элементов.

SVG определяет векторную графику в XML, которую можно напрямую встраивать в HTML-страницы. Графика SVG масштабируема и не теряет качества при масштабировании или изменении размера.

## Что такое SVG?

- SVG означает масштабируемую векторную графику;
- SVG используется для определения векторной графики для Интернета;
- SVG определяет графику в формате XML;
- Каждый элемент и атрибут в файлах SVG можно анимировать;
- SVG интегрируется с другими стандартами, такими как CSS, DOM, XSL и JavaScript.

## Элемент SVG

Элемент HTML ``<svg>`` представляет собой контейнер для графики SVG. В SVG есть несколько методов рисования контуров, прямоугольников, кругов, многоугольников, текста и много другого.

### SVG-круг

```
<svg width="100" height="100">
    <circle cx="50" cy="50" r="40" stroke="green" stroke-width="4" fill="yellow">
</svg>
```

### SVG-прямоугольник

```
<svg width="400" height="200">
    <rect x="10" y="10" width="200" height="100" stroke="red" stroke-width="6" fill="blue">
</svg>
```

### Прямоугольник SVG с непрозрачностью и закругленными углами

```
<svg width="400" height="180">
    <rect x="50" y="20" rx="20" ry="20" width="150" height="150" style="fill:red;stroke:black;stroke-width:5;opacity:0.5" />
</svg>
```

### SVG-звезда

```
<svg width="300" height="200">
    <polygon points="100,10 40,198 190,78 10,78 160,198"
            style="fill:lime;stroke:purple;stroke-width:5;fill-rule:evenodd;" />
</svg>
```

### Эллипс градиента SVG и текста

```
<svg height="130" width="500">
    <defs>
        <linearGradient id="grad1">
            <stop offset="0%" stop-color="yellow" />
            <stop offset="100%" stop-color="red" />
        </linearGradient>
    </defs>
    <ellipse cx="100" cy="70" rx="85" ry="55" fill="url(#grad1)" />
    <text fill="#ffffff" font-size="45" font-family="Verdana" x="50" y="86">SVG</text>
    Sorry, your browser does not support inline SVG.
</svg>
```

## Различия между SVG и Canvas

SVG - это язык описания 2D-графики в XML, а Canvas рисует 2D-графику "на лету" (с помощью JavaScript).

SVG основан на XML, а это означает, что каждый элемент доступен в SVG DOM. Вы можете прикрепить обработчики событий JavaScript к графике SVG.

В SVG каждая нарисованная фигура запоминается как объект. Если атрибуты объекта SVG изменяются, браузер может автоматически повторно отобразить форму.

Холст визуализируется попиксельно. В холсте после рисования графика браузер забывает о ней. Если его положение необходимо изменить, необходимо перерисовать всю сцену, включая любые объекты, которые могли бы закрыты графикой.

## Заключение

HTML SVG предоставляет богатый инструментарий для создания векторных изображений, анимации и интерактивных элементов на веб-страницах. Этот мощный инструмент позволяет вам добавлять креативные и динамичные визуальные элементы, делая ваш сайт более привлекательным и интересным для посетителей. Не стесняйтесь использовать HTML SVG для реализации ваших творческих идей и создания визуально привлекательного контента.