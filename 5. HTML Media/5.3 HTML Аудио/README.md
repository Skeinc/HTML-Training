# HTML Audio

Тег `<audio>` воспроизводит звуковые файлы.

← [HTML Media](../README.md) · [Видео](../5.2%20HTML%20%20Видео/README.md)

- [Пример](#пример)
- [Атрибуты](#атрибуты)
- [Дальше](#дальше)

## Пример

```html
<audio controls>
    <source src="song.ogg" type="audio/ogg">
    <source src="song.mp3" type="audio/mpeg">
    <p><a href="song.mp3">Скачать аудио</a></p>
</audio>
```

Пишите `<source>`, не опечатку `sourse`.

## Атрибуты

Те же идеи, что у `<video>`: `controls`, `autoplay`, `muted`, `loop`, `preload`.

```html
<audio controls preload="metadata" src="podcast.mp3"></audio>
```

`autoplay` без `muted` в большинстве браузеров заблокирован.

## Дальше

- [Обзор форматов](../5.1%20HTML%20Медиа/README.md)
- [Справочник: audio](../../HTML%20Reference/HTML%20Tags/Audio%20and%20Video/Tag%20%3Caudio%3E/README.md)
