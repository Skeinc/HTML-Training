# Встраивание YouTube

Видео с YouTube (и похожих платформ) вставляют через **`<iframe>`**, не скачивая файл.

← [HTML Media](../README.md) · [iframe](../../2.%20Basic%20HTML/2.19%20HTML%20Iframes/README.md)

- [Embed-код](#embed-код)
- [Параметры URL](#параметры-url)
- [Практика](#практика)

## Embed-код

ID видео — часть URL после `v=`:

`https://www.youtube.com/watch?v=dQw4w9WgXcQ` → ID `dQw4w9WgXcQ`

```html
<iframe
    width="560"
    height="315"
    src="https://www.youtube.com/embed/dQw4w9WgXcQ"
    title="Название ролика"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen
    loading="lazy"
></iframe>
```

`title` обязателен для доступности.

## Параметры URL

Добавляются к `src` через `?` и `&`:

| Параметр | Эффект |
|----------|--------|
| `autoplay=1` | Автостарт (часто с `mute=1`) |
| `mute=1` | Без звука |
| `start=30` | Начать с 30-й секунды |
| `rel=0` | Меньше похожих (ограниченно) |

```
https://www.youtube.com/embed/ID?mute=1&autoplay=1
```

## Практика

- Не автозапускайте со звуком — раздражает и блокируется
- Адаптивная обёртка: CSS `aspect-ratio: 16/9` + `width: 100%`
- Для продакшена смотрите политику cookies/privacy (youtube-nocookie.com)

## Дальше

- [Видео своих файлов](../5.2%20HTML%20%20Видео/README.md)
