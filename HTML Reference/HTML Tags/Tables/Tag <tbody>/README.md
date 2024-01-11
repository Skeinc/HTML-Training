# Тег tbody

Тег ``<tbody>`` в HTML предоставляет собой контейнерный элемент, используемый для группировки строк с данными внутри таблицы. Этот тег обычно следует за ``<thead>`` (если присутствует) и содержит основное тело таблицы с фактическими данными.

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tag tbody</title>
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

Тег ``<tbody>`` используется для группировки содержимого тела в таблице HTML. Этот ``<tbody>`` элемент используется вместе с элементами ``<thead>`` и ``<tfoot>`` для указания каждой части таблицы (тело, заголовок, нижний колонтитул).

Браузеры могут использовать эти элементы для прокрутки тела таблицы независимо от верхнего и нижнего колонтитула. Кроме того, при печати большой таблицы, занимающей несколько страниц, эти элементы позволяют печатать верхний и нижний колонтитулы таблицы вверху и внизу каждой страницы.

**Примечание:** Внутри элемента ``<tbody>`` должен быть один или несколько тегов ``<tr>``.

Тег ``<tbody>`` необходимо использовать в следующем контексте: в качестве дочернего элемента ``<table>``, после любых элементов ``<caption>``, ``<colgroup>`` и ``<thead>``.

## Примечания

- Элементы ``<thead>``, ``<tbody>`` и ``<toot>`` по умолчанию не влияют на макет таблицы. Однако вы можете использовать CSS для стилизации этих элементов;
- Тег ``<tbody>`` поддерживает глобальные атрибуты в HTML;
- Тег ``<tbody>`` поддерживает атрибуты событий в HTML.

## Настройки CSS по умолчанию

Большинство браузеров отображают ``<tbody>`` элемент со следующими значениями по умолчанию:

```
tbody {
    display: table-row-group;
    vertical-align: middle;
    border-color: inherit;
}
```

## Заключение

Тег ``<tbody>`` в HTML помогает структурировать и организовывать фактические данные внутри таблицы. Правильное использование этого тега способствует улучшению читаемости и обслуживания ваших таблиц.