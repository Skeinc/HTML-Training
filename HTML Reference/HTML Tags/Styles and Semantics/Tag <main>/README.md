# Тег main

Тег ``<main>`` является семантическим тегом HTML5 и используется для определения основного содержания веб-страницы. Тег ``<main>`` предназначен для определения основной части содержания веб-страницы. Он объединяет в себе главный контент, и его использование способствует более явному выделению ключевого контента на странице.

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tag main</title>
</head>
<body>
    <main>
        <h1>Most Popular Browsers</h1>
        <p>Chrome, Firefox, and Edge are the most used browsers today.</p>

        <article>
            <h2>Google Chrome</h2>
            <p>Google Chrome is a web browser developed by Google, released in 2008.</p>
        </article>

        <article>
            <h2>Mozzila Firefox</h2>
            <p>Mozilla Firefox is an open-source web browser developed by Mozilla.</p>
        </article>

        <article>
            <h2>Microsoft Edge</h2>
            <p>Miscrosoft Edge is a web browser developed by Microsoft, released in 2015.</p>
        </article>
    </main>
</body>
</html>
```

## Определение и использование

Тег ``<main>`` определяет основное содержимое документа. Содержимое внутри ``<main>`` элемента должно быть уникальным для документа. Он не должен содержать контент, повторяющийся в документах, например боковые панели, навигационные ссылки, информацию об авторских правах, логотипы сайтов и формы поиска.

## Примечания

- В документе не должно быть более одного элемента ``<main>``. Элемент ``<main>`` не должен быть потомком элемента ``<article>``, ``<aside>``, ``<footer>``, ``<header>`` или ``<nav>``;
- Тег ``<main>`` поддерживает глобальные атрибуты в HTML;
- Тег ``<main>`` поддерживает атрибуты событий в HTML.

## Заключение

Тег ``<main>`` предоставляет удобный и семантический способ выделения основного содержания на веб-странице. Используйте его для обозначения ключевого контента, который составляет ядро вашей страницы. Это способствует лучшей структуре документа, повышает его доступность и улучшает восприятие контента  браузерами и поисковыми системами.