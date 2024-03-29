# Тег thead

Тег ``<thead>`` в HTML представляет собой контейнерный элемент, который используется для группировки заголовков столбцов внутри таблицы. Этот тег обычно располагается перед телом таблицы (``<tbody>``) и после заголовка таблицы (``<caption>``), если таковой имеется.

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tag thead</title>
    <style>
        table {
            width: 100%;
        }
        td {
            text-align: center;
        }
        table,th,td {
            border: 1px solid black;
            border-collapse: collapse;
        }
    </style>
</head>
<body>
    <table>
        <thead>
            <tr>
                <th>Month</th>
                <th>Savings</th>
            </tr>
        </thead>

        <tbody>
            <tr>
                <td>January</td>
                <td>$100</td>
            </tr>
            <tr>
                <td>February</td>
                <td>$80</td>
            </tr>
        </tbody>

        <tfoot>
            <tr>
                <td>Summary</td>
                <td>$180</td>
            </tr>
        </tfoot>
    </table>
</body>
</html>
```

## Определение и использование

Тег ``<thead>`` используется для группировки содержимого заголовка в таблице HTML. Этот ``<thead>`` элемент используется вместе с элементами ``<tbody>`` и ``<tfoot>`` для указания каждой части таблицы (заголовок, тело, нижний колонтитул).

Браузеры могут использовать эти элементы для прокрутки тела таблицы независимо от верхнего и нижнего колонтитула. Кроме того, при печати большой таблицы, занимающей несколько страниц, эти элементы позволяют печатать верхний и нижний колонтитулы таблицы вверху и внизу каждой страницы.

**Примечание:** Внутри элемента ``<thead>`` должен быть  один или несколько тегов ``<tr>``.

Тег ``<thead>`` необходимо использовать в следующем контексте: в качестве дочернего элемента ``<table>``, после любых элементов ``<caption>`` и ``<colgroup>``, и перед любыми элементами ``<tbody>``, ``<tfoot>``, ``<tr>``.

## Примечания

- Тег ``<thead>`` поддерживает глобальные атрибуты в HTML;
- Тег ``<thead>`` поддерживает атрибуты событий в HTML.

## Настройки CSS по умолчанию

Большинство браузеров отображают ``<thead>`` элемент со следующими значениями по умолчанию:

```
thead {
    display: table-header-group;
    vertical-align: middle;
    border-color: inherit;
}
```

## Заключение

Тег ``<thead>`` в HTML предоставляет эффективный способ группировки и выделения заголовков столбцов в таблице. Правильное использование этого тега улучшает читаемость и структурированность ваших таблиц.