# HTML-объекты

HTML-объекты представляют собой специальные коды, которые используются для представления символов, которые имеют специальное значение в HTML.

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML Entities</title>
</head>
<body>
    <h1>Some HTML Character Entities</h1>
    <p>Non-breaking space sign: &nbsp;</p>
    <p>Less than sign: &lt;</p>
    <p>Greater than sign: $gt;</p>
    <p>Ampersand than sign: &amp;</p>
    <p>Double quotation mark sign: &quot;</p>
    <p>Single quotation mark sign: &apos;</p>
    <p>Cent sign: &cent;</p>
    <p>Pound sign: &pound;</p>
    <p>Yen sign: &yen;</p>
    <p>Euro sign: &euro;</p>
    <p>Copy sign: &copy;</p>
    <p>Trademark sign: &reg;</p>
</body>
</html>
```

Некоторые символы зарезервированы в HTML. Если вы используете знаки "меньше" или "больше" в тексте HTML, браузер может смешивать их с тегами. Имена или номера объектов можно использовать для отображения зарезервированных символов HTML.

Имена сущностей выглядят следующим образом:

```
&entity_name
```

Номера сущностей выглядят следующим образом:

```
&#entity_number
```

Чтобы отобразить знак меньше, мы должны написать &lt;

## Зачем нужны HTML-символы

- **Экранирование символов:** HTML использует определенные символы для форматирования документа. Однако, если мы хотим использовать сами эти символы в тексте без какого-либо форматирования, нам нужно использовать HTML-символы для представления этих символов.
- **Поддержка различных символов:** HTML-символы также полезны, когда мы хотим вставить специальные символы, которые не могут быть просто введены с клавиатуры.

## Неразрывное пространство

Обычно используемым объектом HTML является неразрывный пробел:

*Неразрывный пробел* - это пробел, который не переходит на новую строку. Два слова, разделенные неразрывным пробелом, будут слипаться. Это удобно, когда нарушение слов может помешать.

Два слова, разделенные неразрывным пробелом, будут слипаться (не переходить на новую строку). Это удобно, когда нарушение слов может помешать.

Другое распространенное использование неразрывного пространства - запрет браузерам обрезать пробелы на страницах HTML.

Если вы напишите в тексте 10 пробелов, браузер удалит 9 из них. Чтобы добавить в текст пробелы, вы можете использовать сущность персонажа.

## Объединение диакритических знаков

Диакритический знак - это "глиф", добавляемый к букве. Некоторые диакритические знаки, такие как серьезный и острый, называются акцентами.

Диакритические знаки можно использовать в сочетании с буквенно-цифровыми символами для создания символа, которого нет в наборе символов (кодировке), используемом на странице.

## Заключение

HTML-объекты - это мощный инструмент для работы с текстом в HTML. Они помогают избежать конфликтов с зарезервированными символами, предоставляя способ вставки специальных символов и обеспечивая корректное отображение текста.