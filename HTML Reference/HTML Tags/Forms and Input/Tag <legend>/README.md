# Тег legend

Тег ``<legend>`` в HTML предназначен для создания заголовка или описания для группы связанных элементов формы, заключенных внутри тега ``<fieldset>``. Этот тег способствует лучшей структурированности форм и улучшению их доступности.

Тег ``<legend>`` следует после открывающего тега ``<fieldset>`` и предоставляет текстовую метку, которая описывает группу элементов формы, находящихся внутри ``<fieldset>``.

Пример:

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tag legend</title>
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

Тег ``<legend>`` определяет заголовок для элемента ``<fieldset>``.

## Примечания

- Тег ``<legend>`` поддерживает глобальные атрибуты в HTML;
- Тег ``<legend>`` поддерживает атрибуты событий в HTML.

## Настройки CSS по умолчанию

Большинство браузеров отображают ``<legend>`` элемент со следующими значениями по умолчанию:

```
legend {
    display: block;
    padding-left: 2px;
    padding-right: 2px;
    border: none;
}
```

## Заключение

Тег ``<legend>`` в HTML является важным инструментом для создания читаемых и доступных форм. Используйте его для ясного и информативного описания групп элементов формы, делая ваш интерфейс более понятным и удобным для пользователей.