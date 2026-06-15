# HTML Video

Тег `<video>` воспроизводит видеофайлы на странице.

← [HTML Media](../README.md) · [Аудио](../5.3%20HTML%20Аудио/README.md)

- [Базовый пример](#базовый-пример)
- [Атрибуты](#атрибуты)
- [Субтитры](#субтитры)
- [Дальше](#дальше)

## Базовый пример

```html
<video width="640" height="360" controls poster="preview.jpg">
    <source src="movie.webm" type="video/webm">
    <source src="movie.mp4" type="video/mp4">
    <p>Ваш браузер не поддерживает видео. <a href="movie.mp4">Скачать</a></p>
</video>
```

`width`/`height` снижают скачок вёрстки при загрузке. `poster` — картинка до воспроизведения.

## Атрибуты

| Атрибут | Назначение |
|---------|------------|
| `controls` | Панель play/pause/громкость |
| `autoplay` | Автостарт (обычно только с `muted`) |
| `muted` | Без звука |
| `loop` | Зацикливание |
| `playsinline` | Воспроизведение inline на iOS |
| `preload` | `none` \| `metadata` \| `auto` |

```html
<video autoplay muted loop playsinline src="bg.mp4"></video>
```

## Субтитры

```html
<video controls>
    <source src="lecture.mp4" type="video/mp4">
    <track kind="subtitles" src="ru.vtt" srclang="ru" label="Русский" default>
</video>
```

Формат субтитров — WebVTT (`.vtt`). `kind`: `subtitles`, `captions`, `descriptions`.

## Дальше

- [YouTube embed](../5.5%20HTML%20Youtube%20Videos/README.md)
- [Основы доступности](../../6.%20HTML%20Accessibillity/6.1%20HTML%20Accessibility%20Basics/README.md)
