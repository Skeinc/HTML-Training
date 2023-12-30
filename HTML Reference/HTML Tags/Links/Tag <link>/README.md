# Тег link

Тег ``<link>`` используется для связывания веб-страницы с внешними ресурсами, такими как CSS, иконки, а также установки связей с другими документами. Тег ``<link>`` представляет собой пустой элемент, котоырй используется для связывания внешних ресурсов с веб-страницей. Он чаще всего используется для подключения стилей CSS к HTML-документу.

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tag link</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    
</body>
</html>
```

В данном примере тег ``<link>`` используется для подключения внешнего файла стилей **style.css** к веб-странице.

## Атрибуты

- **crossorigin:** anonymous, use-credentials | Указывает, как элемент обрабатывает запросы с другого источника.
- **href:** URL | Указывает местоположение связанного документа.
- **hreflang:** language_code | Указывает язык связанного документа.
- **media:** media_query | Указывает на то, на каком устройстве будет отображен связанный документ.
- **referrerpolicy:** no-referrer, no-referrer-when-downgrade, orogin, origin-when-cross-origin, same-origin, strict-origin-when-cross-origin, unsafe-url | Указывает, какой реферер использовать при получении ресурса.
- **rel:** alternate, author, dns-prefetch, help, icon, license, next, pingback, preconnect, prefetch, preload, prev, search, stylesheet | Обязательно. Указывает отношение между текущим документом и связанным документом.
- **sizes:** Height x Width | Указывает размер связанного ресурса. Только для rel="icon".
- **title:** | Определяет предпочтительный или альтернативный стиль таблицы стилей.
- **type:** media_type | Указывает тип медиафайла, связанного с документом.

## Примечания

- Элемент ``<link>`` является пустым элементом и содержит только атрибуты.
- Тег ``<link>`` поддерживает глобальные атрибуты в HTML.
- Тег ``<link>`` поддерживает атрибуты событий в HTML.

## Настройки CSS по умолчанию

Большинство браузеров отображают элемент ``<link>`` со следующими значениями по умолчанию:

```
link {
    display: none;
}
```

## Заключение

Тег ``<link>`` в HTML является мощным инструментом для управления внешними ресурсами веб-страницы. Используйте его для подключения стилей, иконок, установки связей с другими документами и обеспечения лучшего пользовательского опыта.