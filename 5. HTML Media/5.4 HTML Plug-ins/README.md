# Плагины (legacy)

Историческая тема: Java-апплеты, Flash, ActiveX, Silverlight. **В современных браузерах не используются.**

← [HTML Media](../README.md)

## Что было

Плагины расширяли браузер внешними программами. Элементы `<object>` и `<embed>` встраивали такой контент.

## Чем заменить сегодня

| Было | Сейчас |
|------|--------|
| Flash-видео | `<video>` + MP4/WebM |
| Flash-игры | Canvas / WebGL |
| PDF-плагин | `<iframe src="doc.pdf">` или PDF.js |
| Java-апплет | Не поддерживается |

```html
<!-- устаревший подход -->
<object data="player.swf" type="application/x-shockwave-flash"></object>
```

## `<object>` сегодня

Редко: вложенный HTML, PDF, SVG. Для своих видео/аудио — `<video>` / `<audio>`.

## Дальше

- [Видео](../5.2%20HTML%20%20Видео/README.md)
- [YouTube](../5.5%20HTML%20Youtube%20Videos/README.md)
