# Тег search

Тег ``<search>`` обычно используется для создания полей ввода на веб-страницах.

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tag search</title>
</head>
<body>
    <search>
        <form>
            <input type="search" name="searchField" id="search" placeholder="Search...">
        </form>
    </search>
</body>
</html>
```

## Определение и использование

Тег ``<search>`` используется для указания того, что здесь находится набор элементов, связанных с поиском. Элементы внутри ``<search>`` элемента обычно могут быть элементами формы, используемыми для выполнения поиска.

## Примечания

- Тег ``<search>`` не отображается в браузере как нечто особенное. Однако вы можете стилизовать при помощи CSS тег ``<search>`` и его содержимое;
- Тег ``<search>`` поддерживает глобальные атрибуты в HTML;
- Тег ``<search>`` поддерживает атрибуты событий в HTML.

## Настройки CSS по умолчанию

Браузеры обычно отоброжают тег ``<search>`` со следующими значениями по умолчанию:

```
search {
    display: block;
}
```

## Заключение

Тег ``<search>`` может понадобится для создания поля поиска. При помощи данного элемента легко создавать функциональные и стилизованные поля поиска на веб-страницах.