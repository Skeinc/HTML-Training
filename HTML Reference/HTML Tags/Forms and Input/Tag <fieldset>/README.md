# Тег fieldset

HTML-тег ``<fieldset>`` представляет собой элемент, используемый для группировки и организации связанных элементов формы. В сочетании с ``<legend>``, ``<fieldset>`` создает блок с заголовком, который помогает лучше структурировать формы на веб-страницах.

Тег ``<fieldset>`` обрамляет группу связанных элементов формы и обеспечивает им визуальное и логическое объединение.

Пример использования тега ``<fieldset>``:

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tag fieldset</title>
</head>
<body>
    <form action="">
        <fieldset>
            <legend>Personalia:</legend>
            <label for="fname">First name:</label><br>
            <input type="text" id="fname" name="fname"><br><br>

            <label for="lname">Last name:</label><br>
            <input type="text" id="lname" name="lname"><br><br>

            <label for="email">Email:</label><br>
            <input type="email" id="email" name="email"><br><br>

            <input type="submit" value="Send">
        </fieldset>
    </form>
</body>
</html>
```

## Определение и использование

Тег ``<fieldset>`` используется для группировки связанных элементов в форме. Тег ``<fieldset>`` рисует рамку вокруг связанных элементов.

## Атрибуты

- **disabled:** disabled | Указывает, что все связанные с ним элементы формы должны быть отключены;
- **form:** form_id | Указывает идентификатор формы;
- **name:** text | Позволяет задать имя для ``<fieldset>``.

## Примечания

- Тег ``<legend>`` используется для определения заголовка элемента ``<fieldset>``;
- Тег ``<fieldset>`` поддерживает глобальные атрибуты в HTML;
- Тег ``<fieldset>`` поддерживает атрибуты событий в HTML.


## Настройки CSS по умолчанию

Большинство браузеров отображают ``<fieldset>`` элемент со следующими значениями по умолчанию:

```
fieldset {
    display: block;
    margin-left: 2px;
    margin-right: 2px;
    padding-top: 0.35em;
    padding-bottom: 0.625em;
    padding-left: 0.75em;
    padding-right: 0.75em;
    border: 2px groove (internal value);
}
```

## Заключение

Тег ``<fieldset>`` является важным элементов для создания структурированных и доступных форм на веб-страницах. Используйте его для группировки и организации связанных элементов формы, делая интерфейс более понятным и удобным для пользователей. Комбинируйте ``<fieldset>`` с ``<legend>`` и стилями для создания эффективных и привлекательных форм.