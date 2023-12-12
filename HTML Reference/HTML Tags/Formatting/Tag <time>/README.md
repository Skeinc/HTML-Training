# Тег time

Тег ``<time>`` предназначен для разметки времени или даты на вашей веб-странице, что не только способствует семантике, но также обеспечивает удобочитаемость и поддержку множества форматов. Тег ``<time>`` используется для обозначения даты или времени в вашем документе. Он может содержать атрибут ``datetime``, который представляет собой машинно-читаемое значение.

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tag time</title>
</head>
<body>
    <p>Open from <time>10:00</time> to <time>21:00</time> every weekday.</p>
    <p>I have a date on <time datetime="2008-02-14 20:00">Valentines day</time>.</p>

    <button onclick="getCurrentDateTime()" type="button">Get current time</button>
    <p>Current time = <time id="currentTime"></time></p>

    <script>
        function getCurrentDateTime() {
            const date = new Date();
            const currentTime = document.getElementById("currentTime");

            function parseMonth(month) {
                if(month == 12) {
                    month = 1;
                }
                else {
                    month++;
                }

                return month;
            }

            currentTime.innerHTML = `${date.getFullYear()}-${parseMonth(date.getMonth())}-${date.getDate()} ${date.getHours()}:${date.getMinutes()}:${date.getSeconds()}`;
        }
    </script>
</body>
</html>
```

## Атрибут datetime

Атрибут ``datetime`` является ключевым для тега ``<time>``. Он используется для предоставления машинно-читаемого представления даты или времени.

## Поддержка интервалов

Тег ``<time>`` также может использоваться для предоставления временных интервалов.

## Примечания

- Тег ``<time>`` поддерживает глобальные атрибуты в HTML.
- Тег ``<time>`` поддерживает атрибуты событий в HTML.

## Заключение

Тег ``<time>`` в HTML предоставляет удобный и семантический способ представления даты и времени. Используйте его для ясного и правильного обозначения моментов в вашем контенте.