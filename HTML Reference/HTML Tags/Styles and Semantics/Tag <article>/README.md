# Тег article

Тег ``<article>`` является семантическим тегом HTML5 и используется для выделения независимого, самостоятельного контента на веб-странице. Тег ``<article>`` предназначен для выделения контента, который является независимым от контекста страницы. Это может быть статья, новость, блоговая запись, комментарий и другие элементы, которые сами по себе составляют логическую единицу.

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tag article</title>
</head>
<body>
    <article>
        <h2>Google Chrome</h2>
        <p>Google Chrome is a web browser developed by Google, released in 2008. Chrome is the world's most popular web browser today!</p>
    </article>
        
    <article>
        <h2>Mozilla Firefox</h2>
        <p>Mozilla Firefox is an open-source web browser developed by Mozilla. Firefox has been the second most popular web browser since January, 2018.</p>
    </article>
        
    <article>
        <h2>Microsoft Edge</h2>
        <p>Microsoft Edge is a web browser developed by Microsoft, released in 2015. Microsoft Edge replaced Internet Explorer.</p>
    </article>
</body>
</html>
```

## Определение и использование

Тег ``<article>`` определяет независимый, автономный контент. Статья должна иметь смысл сама по себе, и ее должна быть возможность распространять независимо от остальной части сайта.

Потенциальные источники элемента ``<article>``:

- Сообщение на форуме;
- Сообщение блога;
- Новостной сюжет.

## Примечания

- Тег ``<article>`` не отображается в браузере как нечто особенное. Однако вы можете использовать CSS для стилизации ``<article>`` элемента;
- Тег ``<article>`` поддерживает глобальные атрибуты в HTML;
- Тег ``<article>`` поддерживает атрибуты событий в HTML.

## Настройки CSS по умолчанию

Большинство браузеров отображают ``<article>`` элемент со следующими значениями по умолчанию:

```
article {
    display: block;
}
```

## Заключение

Тег ``<article>`` предоставляет эффективный способ выделения независимых контентных блоков на веб-странице. Используйте его для статей, новостей, блогов и других элементов, которые могут существовать как самостоятельные единицы контента. Это способствует лучшей организации вашего документа и повышает его семантику и доступность.