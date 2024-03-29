# HTML Аудио

HTML Аудио представляет собой мощный инструмент для встраивания звуковых файлов непосредственно на веб-страницы. С элементом ``<audio>`` HTML5 разработчики получили стандартизированное средство для представления и управления аудио-контентом, обеспечивая при этом совместимость с различными браузерами и платформами.

## Основная структура

Элемент ``<audio>`` легко внедрить в веб-страницу. Вот основная структура:

```
<audio controls>
    <sourse src="example.mp3" type="audio/mpeg">
    Your browser does not support the audio element.
</audio>
```

Атрибут ``controls`` добавляет элементы управления, такие как воспроизведение, пауза и громкость.

Атрибут ``sourse`` предоставляет разные форматы аудио для обеспечения совместимости с различными браузерами.

## HTML Аудио - как это работает?

Атрибут ``controls`` добавляет элементы управления аудиоплеером, такие как воспроизведение, пауза и громкость.

Элемент ``<sourse>`` позволяет указать альтернативные аудиофайлы, из которых браузер может выбрать. Браузер будет использовать первый распознанный формат.

Текст между тегами ``<audio>`` и ``</audio>`` будет отображаться только в браузерах, которые не поддерживают элемент ``<audio>``.

## HTML Аудио - Автовоспроизведение

Чтобы автоматически запустить аудиофайл, используйте ``autoplay`` атрибут:

```
<audio controls autoplay>
    <sourse src="example.mp3" type="audio/mpeg">
    Your browser does not support the audio element.
</audio>
```

**Примечание:** Браузеры Chromium в большинстве случаев не поддерживают автозапуск. Однако отключенный автозапуск всегда разрешен.

Добавьте ``muted`` после ``autoplay``, чтобы ваш аудиофайл начал воспроизводиться автоматически (но без звука):

```
<audio controls autoplay muted>
    <sourse src="example.mp3" type="audio/mpeg">
    Your browser does not support the audio element.
</audio>
```

## HTML-аудиоформаты

Поддерживаются три аудиоформата: MP3, WAV и OGG. Браузер поддерживает различные форматы:

- **Edge:** MP3 - YES, WAV - YES*, Ogg - YES*;

- **Chrome:** MP3 - YES, WAV - YES, Ogg - YES;

- **Firefox:** MP3 - YES, WAV - YES, Ogg - YES;

- **Safari:** MP3 - YES, WAV - YES, Ogg - NO;

- **Edge:** MP3 - YES, WAV - YES, Ogg - YES;

## HTML-аудио - типы мультимедиа

*File Format* - *Media Type*:

- **MP3:** audio/mpeg;

- **OGG:** audio/ogg;

- **WAV:** audio/wav

## HTML Аудио - методы, свойства и события

HTML DOM определяет методы, свойства и события для ``<audio>`` элемента.

Это позволяет загружать, воспроизводить и приостанавливать аудио, а также устанавливать продолжительность и громкость.

Существуют также события DOM, которые могут уведомлять вас, когда звук начинает воспроизводиться, приостанавливается и т.д.

## Заключение

HTML Audio предоставляет удобное и стандартизированное решение для встраивания аудио-контента в веб-страницы. С его поддержкой различных форматов, элементами управления и возможностью программного управления HTML Audio помогает создавать привлекательные аудио-впечатления на веб-страницах. По мере развития веб-технологий, HTML Audio продолжает оставаться важным инструментом для предоставления качественного аудио-контента пользователям на различных устройствах и браузерах.