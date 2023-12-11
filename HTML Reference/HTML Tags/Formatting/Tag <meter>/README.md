# Тег meter

Тег ``<meter>`` представляет собой элемент разметки, используемый для представления значения в заданном диапозоне, такого как измерение или процентное соотношение. Тег ``<meter>``предназначен для отображения значения в заданном диапозоне. Это может быть полезно, например, для показа уровня заполнения прогресс-бара или отображения числовых измерений.

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tag meter</title>
</head>
<body>
    <label for="disk_c">Disk usage C:</label>
    <meter id="disk_c" value="50" min="0" max="100">50%</meter>

    <label for="disk_d">Disk usage D:</label>
    <meter id="disk_d" value="75" min="0" max="100" low="30" high="70" optimum="80">75%</meter>
</body>
</html>
```

## Атрибуты value, min, max

Тег ``<meter>`` использует атрибуты ``value``, ``min`` и ``max`` для определения текущего значения, минимального и максимального пределов. В привиденном выше примере ``value="50"``, ``min="0"``, ``max="100"`` определяют соответственно значение в 50%, минимальное значение 0 и максимальное значение 100.

## Атрибут low, high, optimum

Дополнительные атрибуты ``<meter>`` включают ``low``, ``high``, ``optimum``, которые позволяют установить диапозоны, соответствующие низким, высоким и оптимальным значениям.

## Примечания

- Всегда добавляйте тег ``<label>``, чтобы обеспечить максимальную доступность.
- Тег ``<meter>`` поддерживает глобальные атрибуты в HTML.
- Тег ``<meter>`` поддерживает атрибуты событий в HTML.

## Заключение

Тег ``<meter>`` в HTML предоставляет удобный способ отображения значения в заданном диапозоне на вашем веб-сайте. Используйте его для создания информативных индикаторов, таких как прогресс-бары или измерения процентного соотношения.