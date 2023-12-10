# Тег progress

Тег ``<progress>`` представляет собой элемент разметки, используемый для отображения прогресса выполнения задачи на веб-странице. Тег ``<progress>`` предназначен для представления степени завершенности задачи, например, загрузки ресурсов или выполнения определенного процесса.

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tag progress</title>
</head>
<body>
    <label for="file">Downloading progress:</label>
    <progress id="file" value="62" max="100">62%</progress>
</body>
</html>
```

## Атрибуты value, max

Тег ``<progress>`` использует атрибуты ``value``, ``max`` для определения текущей степени завершенности и максимального значения.

- ``value``: Текущая степень завершенности.
- ``max``: Максимальное значение, которое соответствует 100% выполнения.

## Прогресс с использованием JavaScript

Значение ``<progress>`` можно обновлять динамически с использованием JavaScript для отображения реального прогресса выполнения задачи.

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tag progress</title>
</head>
<body>
    <label for="file">Downloading progress:</label>
    <progress id="file" value="0" max="100">0%</progress>

    <script>
        const progress = document.querySelector('#file');
        let value = 0;

        function updateProgress() {
            value += 1;
            progress.value = value;
            progress.innerHTML = value + "%";

            if(value < 100) {
                setTimeout(updateProgress, 100);
            }
        }

        updateProgress();
    </script>
</body>
</html>
```

## Примечания

- Всегда добавляйте тег ``<label>``, чтобы обеспечить максимальную доступность.
- Используйте ``<progress>`` тег вместе с JavaScript, чтобы отображать ход выполнения задачи.
- Тег ``<progress>`` не подходит для представления показателей (например, использование дискового пространства или релевантности результата запроса). Чтобы представить датчик, используйте вместо него тег ``<meter>``.
- Тег ``<progress>`` поддерживает глобальные атрибуты в HTML.
- Тег ``<progress>`` поддерживает атрибуты событий в HTML.

## Заключение

Тег ``<progress>`` в HTML предоставляет удобный способ отображения прогресса выполнения задачи на вашем веб-сайте. Используйте его для создания информативных индикаторов, например, при загрузке контента или выполнении сложных операций.