# Адаптивная вёрстка

Страница корректно выглядит на телефоне, планшете и десктопе. Основа — viewport + гибкие размеры + media queries.

← [Базовый HTML](../README.md) · [Макет](../2.23%20HTML%20Layout/README.md) · [Изображения](../2.10%20HTML%20Images/README.md)

- [Viewport](#viewport)
- [Гибкие размеры](#гибкие-размеры)
- [Media queries](#media-queries)
- [Изображения](#изображения)
- [Дальше](#дальше)

## Viewport

В каждом `<head>`:

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

Без этого мобильный браузер «сожмёт» десктопную страницу.

## Гибкие размеры

| Приём | Пример |
|-------|--------|
| Проценты | `width: 100%` |
| `max-width` | картинка не шире контейнера |
| `minmax()` в Grid | `grid-template-columns: repeat(auto-fit, minmax(200px, 1fr))` |
| Flexbox | колонки переносятся через `flex-wrap` |

Макет колонок — **Flexbox/Grid**, не `float`.

## Media queries

Стили в зависимости от ширины экрана:

```css
.row { display: flex; gap: 1rem; }

@media (max-width: 768px) {
    .row { flex-direction: column; }
    aside { width: 100%; }
}
```

Типичные breakpoints подбирают под дизайн (не обязательно 768/1024).

## Изображения

```html
<img src="photo.jpg" alt="…" style="max-width: 100%; height: auto;">
```

```html
<picture>
    <source media="(max-width: 600px)" srcset="photo-small.jpg">
    <img src="photo.jpg" alt="…">
</picture>
```

Единица `vw` для текста возможна, но мелкий шрифт на узком экране — проверяйте читаемость.

## Дальше

- [Макет](../2.23%20HTML%20Layout/README.md)
- [CSS-Training](../../CSS-Training/README.md)
