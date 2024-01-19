# HTML элемент div

Тег ``<div>`` (division) представляет собой блочный контейнер в HTML, который исопльзуется для группировки и организации других элементов. Это универсальный инструмент для создания блочной структуры на веб-странице. Элемент ``<div>`` используется как контейнер для других элементов HTML.

## Элемент div

По умолчанию элемент ``<div>`` является блочным, то есть он занимает всю доступную ширину и имеет разрывы строк до и после:

```
<p>Lorem Ipsum <div>I am a div</div> dolor sit amet.</p>
```

Элемент ``<div>`` не имеет обязательных атрибутов, но, например, ``style``, ``class`` и ``id`` являются общими.

## Элемент div как контейнер

Элемент ``<div>`` часто используется для группировки разделов веб-страницы:

```
<div>
    <h2>London</h2>
    <p>London is the capital city of England.</p>
    <p>Londond has over 13 million inhabitants.</p>
</div>
```

## Выравнивание по центру элемент div

Если у вас есть ``<div>`` элемент, ширина которого не равна 100% и вы хотите выровнять его по центру, установите ``margin`` для свойства CSS значение ``auto``:

```
<div style="width: 300px; margin: auto;">
    <h2>London</h2>
    <p>London is the capital city of England.</p>
    <p>Londond has over 13 million inhabitants.</p>
</div>
```

## Несколько элементов div

На одной странице может быть множество контейнеров ``<div>``:

```
<div style="background-color: #FFF4A3;">
    <h2>London</h2>
    <p>London is the capital city of England.</p>
    <p>Londond has over 13 million inhabitants.</p>
</div>

<div style="background-color: #FFC0C7;">
    <h2>Oslo</h2>
    <p>Oslo is the capital city of Norway.</p>
    <p>Oslo has over 600.000 inhabitants.</p>
</div>

<div style="background-color: #D9EEE1;">
    <h2>Rome</h2>
    <p>Rome is the capital city of Italy.</p>
    <p>Rome has over 3 million inhabitants.</p>
</div>
```

## Выравнивание элементов div рядом

При создании веб-страниц часто требуется разместить два или более ``<div>`` элемента рядом. Существуют разные методы выравнивания элементов рядом, все они включают в себя некоторые стили CSS. Мы рассмотрим самые распространенные способы:

### Float

Свойство CSS ``float`` изначально не предназначалось для выравнивания ``<div>`` элементов рядом, но уже много лет используется для этой цели. Свойство CSS ``float`` для позиционирования и форматирования содержимого и позволяет элементам распологаться рядом друг с другом, а не друг над другом.

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML Div</title>
    <style>
        .container__float {
            width: 100%;
            overflow: auto;
        }
        .container__float div {
            width: 33%;
            float: left;
        }
    </style>
</head>
<body>
    <h2>Float</h2>
    <div class="container__float">
        <div style="background-color: #FFF4A3;">
            <h2>London</h2>
            <p>London is the capital city of England.</p>
            <p>Londond has over 13 million inhabitants.</p>
        </div>
    
        <div style="background-color: #FFC0C7;">
            <h2>Oslo</h2>
            <p>Oslo is the capital city of Norway.</p>
            <p>Oslo has over 600.000 inhabitants.</p>
        </div>
    
        <div style="background-color: #D9EEE1;">
            <h2>Rome</h2>
            <p>Rome is the capital city of Italy.</p>
            <p>Rome has over 3 million inhabitants.</p>
        </div>
    </div>
</body>
</html>
```

### Inline-block

Если вы измените свойство ``<div>`` элемента c ``block`` на ``inline-block``, элементы больше не будут добавлять разрыв строки до и после и будут отображаться рядом, а не друг над другом:

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML Div</title>
    <style>
        .container__inline-block {
            width: 30%;
            display: inline-block;
        }
    </style>
</head>
<body>
    <h2>Inline-block</h2>
    <div class="container__inline-block" style="background-color: #FFF4A3;">
        <h2>London</h2>
        <p>London is the capital city of England.</p>
        <p>Londond has over 13 million inhabitants.</p>
    </div>

    <div class="container__inline-block" style="background-color: #FFC0C7;">
        <h2>Oslo</h2>
        <p>Oslo is the capital city of Norway.</p>
        <p>Oslo has over 600.000 inhabitants.</p>
    </div>
</body>
</html>
```

### Flex

Модуль CSS Flexbox Layout был представлен, чтобы упростить разработку гибкой адаптивной структуры макета без использования float или позиционирования. Чтобы метод CSS flex работал, окружите ``<div>`` элементы другим ``<div>`` элементом и присвойте ему статус гибкого контейнера.

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML Div</title>
    <style>
        .container__flex {
            display: flex;
        }
        .container__flex > div {
            width: 33%;
        }
    </style>
</head>
<body>
    <h2>Flex</h2>
    <div class="container__flex">
        <div style="background-color: #FFF4A3;">
            <h2>London</h2>
            <p>London is the capital city of England.</p>
            <p>Londond has over 13 million inhabitants.</p>
        </div>
    
        <div style="background-color: #FFC0C7;">
            <h2>Oslo</h2>
            <p>Oslo is the capital city of Norway.</p>
            <p>Oslo has over 600.000 inhabitants.</p>
        </div>
    
        <div style="background-color: #D9EEE1;">
            <h2>Rome</h2>
            <p>Rome is the capital city of Italy.</p>
            <p>Rome has over 3 million inhabitants.</p>
        </div>
    </div>
</body>
</html>
```

### Grid

Модуль CSS Grid Layout предлагает систему макетов на основе сетки со строками и столбцами, что упрощает разработку веб-страниц без использования плавающих элементов и позиционирования. Звучит почти так же, как flex, но имеет возможность определять более одной строки и позиционировать каждую строку индивидуально. Метод CSS-сетки требует, чтобы вы окружили ``<div>`` элементы другим ``<div>`` элементом и присвоили статус контейнера сетки, а также указали ширину каждого столбца.

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML Div</title>
    <style>
        .container__grid {
            display: grid;
            grid-template-columns: 33% 33% 33%;
        }
    </style>
</head>
<body>
    <h2>Grid</h2>
    <div class="container__grid">
        <div style="background-color: #FFF4A3;">
            <h2>London</h2>
            <p>London is the capital city of England.</p>
            <p>Londond has over 13 million inhabitants.</p>
        </div>
    
        <div style="background-color: #FFC0C7;">
            <h2>Oslo</h2>
            <p>Oslo is the capital city of Norway.</p>
            <p>Oslo has over 600.000 inhabitants.</p>
        </div>
    
        <div style="background-color: #D9EEE1;">
            <h2>Rome</h2>
            <p>Rome is the capital city of Italy.</p>
            <p>Rome has over 3 million inhabitants.</p>
        </div>
    </div>
</body>
</html>
```

## Заключение

Тег ``<div>`` является основным строительным блоком для создания структуры веб-страниц и управления их визуальным представлением. Правильное использование ``<div>`` способствует удобству в разработке, обслуживании и стилизации ваших веб-проектов.