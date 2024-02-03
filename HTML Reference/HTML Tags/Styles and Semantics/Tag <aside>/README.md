# Тег aside

Тег ``<aside>`` является семантическим тегом HTML5 и используется для выделения контента, который является вспомогательным или второстепенным для основного контента страницы. Тег ``<aside>`` предназначен для выделения контента, который является второстепенным или вспомогательным для основного содержимого страницы. Обычно внутри ``<aside>`` размещаются боковые панели, блоки с рекламой, сноски, архивы или другие элементы, которые не являются неотъемлемой частью основного контента.

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tag aside</title>
</head>
<body>
    <p>My family and I visited The Epcot center this summer. The weather was nice, and Epcot was amazing! I had a great summer together with my family!</p>

    <aside>
        <h4>Epcot Center</h4>
        <p>Epcot is a theme park at Walt Disney World Resort featuring exciting attractions, international pavilions, award-winning fireworks and seasonal special events.</p>
    </aside>
</body>
</html>
```

## Определение и использование

Тег ``<aside>`` определяет некоторый контент, помимо контента, в котором он размещен. Сторонний контент должен быть косвенно связан с окружающим контентом. Содержимое ``<aside>`` часто размещается в виде боковой панели документа.

## Примечания

- Тег ``<aside>`` не отображается в браузере как нечто особенное. Однако вы можете использовать CSS для стилизации ``<aside>`` элемента;
- Тег ``<aside>`` поддерживает глобальные атрибуты в HTML;
- Тег ``<aside>`` поддерживает атрибуты событий в HTML.

## Настройки CSS по умолчанию

Большинство браузеров отображают ``<aside>`` элемент со следующими значениями по умолчанию:

```
aside {
    display: block;
}
```

## Заключение

Тег ``<aside>`` предоставляет средство выделения второстепенного контента на веб-странице. Используйте его для боковых панелей, блоков с дополнительной информацией или любого контента, который не является основным, но при этом может быть полезным для посетителей вашего сайта. Это способствует лучшей организации контента и повышает семантику.