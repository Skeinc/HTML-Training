# Тег ol

Тег ``<ol>`` предназначен для создания упорядоченных списков, где порядок элементов имеет значение.

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tag ol</title>
</head>
<body>
    <ol>
        <li>Coffee</li>
        <li>Tea</li>
        <li>Milk</li>
    </ol>

    <ol start="100">
        <li>Coffee</li>
        <li>Tea</li>
        <li>Milk</li>
    </ol>
</body>
</html>
```

## Определение и использование

Тег ``<ol>`` определяет упорядоченный список. Упорядоченный список может быть числовым или алфавитным. Тег ``<li>`` используется для определения каждого элемента списка. Этот тег позволяет структурировать информацию в порядке, который имеет значение для представления контента.

## Атрибуты

- **reversed:** reversed | Указывает, что список будет перевернут;
- **start:** number | Задает начальное значение упорядоченного списка;
- **type:** 1, A, a, I, i | Указывает, какой вид маркера использовать в списке;

## Примечания

- Тег ``<ol>`` поддерживает глобальные атрибуты в HTML;
- Тег ``<ol>`` поддерживает атрибуты событий в HTML.

## Настройки CSS по умолчанию

Большинство браузеров отображают ``<ol>`` элемент со следующими значениями по умолчанию:

```
ol {
    display: block;
    list-style-type: decimal;
    margin-top: 1em;
    margin-bottom: 1em;
    margin-left: 0;
    margin-right: 0;
    padding-left: 40px;
}
```

## Заключение

Тег ``<ol>`` предоставляет отличный способ организации информации с учетом порядка. Экспериментируйте с различными типами маркеров и стилями, чтобы сделать ваш контент более наглядным и интересным.