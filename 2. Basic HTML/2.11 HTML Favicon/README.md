# HTML Favicon

Favicon (Favorites icon) - это небольшая иконка, отображаемая в адресной строке браузера рядом с названием веб-сайта или в закладках. В HTML, добавление favicon - это простой способ придать вашему веб-проекту индвидуальность.

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML Favicon</title>
    <link rel="shortcut icon" href="./image.jpg" type="image/x-icon">
</head>
<body>
    
</body>
</html>
```

## Как добавить значок в HTML

1. **Тег link:** Для подключения favicon к HTML используется тег ``<link>`` с атрибутом ``rel="icon"``. Обычно favicon представлен в формате .ico, но также может быть изображен в форматах PNG, GIF, JPEG.

2. **Apple Touch Icon:** Для улучшения отображения на устройствах Apple, таких как iPhone, iPad и т.д., вы можете добавить тег ``<link>`` с атрибутом ``rel="apple-touch-icon"``.

3. **Динамическое изменение Favicon:** С помощью JavaScript вы можете изменять Favicon динамически, например, при появлении уведомлений.

## Заключение

Добавление favicon - это простой, но важный шаг для создания уникального визуального стиля вашего веб-проекта. Убедитесь, что ваша икона хорошо различима и передает суть вашего сайта. Помните, что файл favicon.ico должен быть размещен в корне вашего проекта.