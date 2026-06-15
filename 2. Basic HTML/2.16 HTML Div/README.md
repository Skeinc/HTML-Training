# Элемент `div`

Универсальный **блочный** контейнер без собственной семантики. Группирует элементы для стилей и скриптов.

← [Базовый HTML](../README.md) · [Блок и inline](../2.15%20Block%20and%20Inline/README.md) · [Семантика](../2.26%20HTML%20Semantics/README.md)

- [Использование](#использование)
- [Макет колонок](#макет-колонок)
- [Когда не `div`](#когда-не-div)

## Использование

```html
<div class="card">
    <h2>Заголовок карточки</h2>
    <p>Текст карточки.</p>
</div>
```

Частые атрибуты: `class`, `id`, `lang`. Не вкладывайте `<div>` внутрь `<p>`.

Центрирование блока фиксированной ширины:

```css
.wrapper { width: 320px; margin: 0 auto; }
```

## Макет колонок

Для колонок рядом используйте **Flexbox** или **Grid** (не `float`):

```html
<div class="row">
    <div class="col">Колонка 1</div>
    <div class="col">Колонка 2</div>
</div>
```

```css
.row { display: flex; gap: 16px; }
.col { flex: 1; }
```

Подробнее — [Макет](../2.23%20HTML%20Layout/README.md). Полные примеры — в [`index.html`](index.html).

## Когда не `div`

Если есть смысловой тег — используйте его:

| Вместо | Лучше |
|--------|-------|
| `<div class="header">` | `<header>` |
| `<div class="nav">` | `<nav>` |
| `<div class="main">` | `<main>` |
| `<div class="footer">` | `<footer>` |

## Дальше

- [Семантика](../2.26%20HTML%20Semantics/README.md)
- [Классы](../2.17%20HTML%20Classes/README.md)
