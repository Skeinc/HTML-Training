# Тег footer

Тег ``<footer>`` является семантическим HTML5 и предназначен для определения нижней части веб-страницы. Тег ``<footer>`` используется для определения футера веб-страницы или раздела. Этот тег содержит информацию, которая обычно располагается в нижней части страницы, такую как копирайт, ссылки на социальные сети, контактная информация или другие важные элементы.

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tag footer</title>
</head>
<body>
    <footer>
        <p>Author: Anufriev Dmitry</p>
        <p><a href="maiilto:iamskezy@gmail.com">hege@example.com</a></p>
    </footer>
</body>
</html>
```

## Определение и использование

Тег ``<footer>`` определяет нижний колонтитул документа или раздела. Элемент ``<footer>`` обычно содержит:

- информация об авторстве;
- информация об авторских правах;
- Контактная информация;
- карта сайта;
- вернуться к началу ссылок;
- связанные документы.

В одном документе может быть несколько ``<footer>`` элементов.

## Примечания

- Контактная информация внутри ``<footer>`` элемента должна находиться внутри тега ``<address>``;
- Тег ``<footer>`` поддерживает глобальные атрибуты в HTML;
- Тег ``<footer>`` поддерживает атрибуты событий в HTML.

## Настройки CSS по умолчанию

Большинство браузеров отображают ``<footer>`` элемент со следующими значениями по умолчанию:

```
footer {
    display: block;
}
```

## Заключение

Тег ``<footer>`` является важным элементов HTML, который предоставляет структурированное место для размещения информации в нижней части веб-страницы. Используйте его для отображения копирайтов, контактная информации и других элементов, которые должны быть видны в конце страницы. Помните также о стилизации и семантике для лучшего восприятия и доступности вашего контента.