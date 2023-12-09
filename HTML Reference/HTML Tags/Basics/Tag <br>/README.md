# Тег br

HTML тег ``<br>`` - это небольшой, но могущественный инструмент для создания переносов и разрывов в тексте. Тег ``<br>`` представляет собой одиночный тег (self-closing), который не имеет закрывающего тега. Его основное предназначение - вставка переносов строки в текстовом контенте:

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tag br</title>
</head>
<body>
    <p>Это текст первой строки.<br>Это текст второй строки.</p>
</body>
</html>
```

## Роль тега в HTML

1. **Перенос текста:** Основная цель тега ``<br>`` - обеспечить перенос текста на новую строку, не создавая новый блок. Это полезно, например, когда вам нужно разделить адрес на несколько строк.
2. **Разрыв блочного элемента:** Тег ``<br>`` может использоваться внутри блочных элементов, чтобы создать разрыв в тексте внутри этого блока.
3. **Разрыв внутри строки:** В теге ``<pre>`` (предварительно форматированный текст), ``<br>`` создает разрыв внутри строки, сохраняя пробелы и переносы строки так, как они записаны в исходном коде.

## Примечания

- Избегайте чрезмерного использования тега ``<br>``. В большинстве случаев для создания разрывов в тексте, лучше использовать блочные элементы и стили.
- Используйте ``<br>`` только для семантических переносов, когда это действительно необходимо в контексте вашего документа.
- Часто тег ``<br>`` используется в комбинации с CSS для более тонкого управления отступами и разрывами.
- Тег ``<br>`` поддерживает глобальные атрибуты в HTML.
- Тег ``<br>`` поддерживает атрибуты событий в HTML.

## Заключение

Тег ``<br>`` может быть мощным средством для создания переносов и разрывов в вашем текстовом контенте. Однако, его следует использовать с умеренностью, придерживаясь семантического подхода и комбинируя с CSS для более гибкого управления оформлением.