# Тег s

Тег ``<s>`` используется для обозначения текста, который представляет собой неактуальную или перечеркнутую информацию. Тег ``<s>`` представляет собой строчный элемент, который создает перечеркнутый текст внутри него.

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tag s</title>
</head>
<body>
    <p><s title="Sorry, 0 tickets left!">ONLY 50 TICKETS LEFT!</s></p>
    <p>SOLD OUT!</p>
</body>
</html>
```

## Зачем использовать тег s?

Тег ``<s>`` обычно используется для пометки текста как зачеркнутого с тем, чтобы указать, что эта информация устарела или неактуальна. Он может быть использован в комбинации с другими элементами или атрибутами для предоставления дополнительной информации.

## Атрибут title

Тег ``<s>`` может использовать атрибут ``title``, чтобы предоставить дополнительные пояснения почему текст был зачеркнут.

## Примечания

- Тег ``<s>`` указывает текст, который больше не является правильным, точным или актуальным. Текст будет отображаться через линию.
- Тег ``<s>`` не следует использовать для определения удаленного текста в документе, для этого используйте тег ``<del>``.
- Тег ``<s>`` поддерживает глобальные атрибуты в HTML.
- Тег ``<s>`` поддерживает атрибуты событий в HTML.

## Настройки CSS по умолчанию

Большинство браузеров отображают ``<s>`` элемент со следующими значениями по умолчанию:

```
s {
    text-decoration: line-through;
}
```

## Заключения

Тег ``<s>`` в HTML предоставляет простой способ отметить текст как неактуальный или устаревший, добавляя эффект перечеркивания. Используйте его, чтобы явно указать на изменения в информации на вашем веб-сайте.