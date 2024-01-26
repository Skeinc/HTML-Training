# HTML-макет

Разработка эффективного макета является ключевым этапов в создании веб-страниц, и HTML предоставляют различные инструменты для организации и структурирования содержимого страницы.

Макет определяет структуру и расположение элементов на веб-странице. Он играет важную роль в создании приятного пользовательского опыта.

Основной структурой веб-страницы является разделение ее на блоки, такие как заголовок (``<header>``), навигация (``<nav>``), основное содержание (``<main>``), боковая панель (``<aside>``), подвал (``<footer>``) и другие.

Теги секции HTML, такие как ``<section>``, ``<article>``, ``<aside>``, предоставляют структуру для лучшего организации содержимого.

## Элементы HTML-макета

HTML имеет несколько семантических элементов, которые определяют различные части веб-страницы:

- header: определяет заголовок документа или раздела;
- nav: определяет набор навигационных ссылок;
- section: определяет раздел в документе;
- article: определяет независимый, самодостаточный контент;
- aside: определяет контент отдельно от контента (например, боковая панель);
- footer: определяет нижний колонтитул документа или раздела;
- details: определяет дополнительные детали, которые пользователь может открывать и закрывать по требованию;
- summary: определяет заголовок для ``<details>`` элемента.

## Методы HTML-разметки

Существует четыре различных метода создания многоколоночных макетов. Каждая техника имеет свои плюсы и минусы:

- CSS-фреймворк;
- CSS-свойство float;
- CSS-flexbox;
- CSS-grid.

## CSS-фреймворки

Если вы хотите быстро создать макет, вы можете использовать платформу CSS, например Bootstrap.

## CSS-float

Обычно целые веб-макеты создаются с использованием ``float`` свойства CSS. Научиться плавать легко - вам просто нужно запомнить, как работают свойства ``float`` и ``clear``.

**Недостатки:** Плавающие элементы привязаны к потоку документов, что может снизить гибкость.

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML Layout</title>
    <style>
        * {
            box-sizing: border-box;
        }

        .full-screen {
            width: 100%;
            height: auto;
        }

        .float-header {
            background-color: rgb(32, 32, 32);
            padding: 30px;
            text-align: center;
            color: white;
        }

        .float-nav {
            float: left;
            width: 30%;
            height: 300px;
            background-color: rgb(152, 152, 152);
        }

        .float-nav ul {
            list-style-type: none;
            padding: 0;
        }

        .float-article {
            float: left;
            padding: 20px;
            width: 70%;
            height: 300px;
            background-color: rgb(200, 200, 200);
        }

        section::after {
            content: "";
            display: table;
            clear: both;
        }

        .float-footer {
            background-color: rgb(32, 32, 32);
            padding: 20px;
            text-align: center;
            color: white;
        }
    </style>
</head>
<body>
    <h1>HTML-Layout</h1>
    <h2>CSS Layout Float</h2>
    <section class="full-screen">
        <header class="float-header">
            <h2>Cities</h2>
        </header>

        <nav class="float-nav">
            <ul>
                <li><a href="#">London</a></li>
                <li><a href="#">Paris</a></li>
                <li><a href="#">Tokyo</a></li>
            </ul>
        </nav>

        <article class="float-article">
            <h3>London</h3>
            <p>London is the capital city of England. It is the most populous city in the  United Kingdom, with a metropolitan area of over 13 million inhabitants.</p>
            <p>Standing on the River Thames, London has been a major settlement for two millennia, its history going back to its founding by the Romans, who named it Londinium.</p>
        </article>

        <footer class="float-footer">
            <p>Nizhny Novgorod, 2024</p>
        </footer>
    </section>
</body>
</html>
```

## CSS-макет Flexbox

Использование flexbox гарантирует предсказуемое поведение элементов, когда макет страницы должен соответствовать разным размерам экрана и различным устройствам отображения.

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML Layout</title>
    <style>
        * {
            box-sizing: border-box;
        }

        .full-screen {
            width: 100%;
            height: auto;
        }

        .flex-container {
            display: flex;
        }

        .flex-header {
            background-color: rgb(32, 32, 32);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            text-align: center;
        }

        .flex-nav {
            background-color: rgb(152, 152, 152);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            color: white;
            width: 30%;
        }

        .flex-nav ul {
            list-style-type: none;
            padding: 0;
        }

        .flex-article {
            background-color: rgb(200, 200, 200);
            display: flex;
            flex-direction: column;
            width: 70%;
            padding: 20px;
        }

        section::after {
            content: "";
            display: table;
            clear: both;
        }

        .flex-footer {
            display: flex;
            justify-content: center;
            align-items: center;
            background-color: rgb(32, 32, 32);
            padding: 20px;
            text-align: center;
            color: white;
        }
    </style>
</head>
<body>
    <h1>HTML-Layout</h1>
    <h2>CSS Flexbox Layout</h2>
    <section class="full-screen">
        <header class="flex-header">
            <h2>Cities</h2>
        </header>

        <div class="flex-container">
            <nav class="flex-nav">
                <ul>
                    <li><a href="#">London</a></li>
                    <li><a href="#">Paris</a></li>
                    <li><a href="#">Tokyo</a></li>
                </ul>
            </nav>
    
            <article class="flex-article">
                <h3>London</h3>
                <p>London is the capital city of England. It is the most populous city in the  United Kingdom, with a metropolitan area of over 13 million inhabitants.</p>
                <p>Standing on the River Thames, London has been a major settlement for two millennia, its history going back to its founding by the Romans, who named it Londinium.</p>
            </article>
        </div>

        <footer class="flex-footer">
            <p>Nizhny Novgorod, 2024</p>
        </footer>
    </section>
</body>
</html>
```

## CSS-Grid

Модуль CSS Grid Layout предлагает систему макетов на основе сетки со строками и столбцами, что упрощает разработку веб-страниц без использования плавающих элементов и позиционирования.

## Заключение

Разработка эффективного макета в HTML и CSS требует понимания структуры страницы и использование различных инструментов, таких как Flexbox и Grid. Отзывчивость и адаптивность становятся все более важными в условиях разнообразия устройств и разрешений экранов.