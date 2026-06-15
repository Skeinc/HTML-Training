# ARIA в HTML

**ARIA** (Accessible Rich Internet Applications) — атрибуты `role` и `aria-*`, которые дополняют разметку для скринридеров и клавиатуры.

← [Доступность](../README.md) · [Основы](../6.1%20HTML%20Accessibility%20Basics/README.md) · [Клавиатура](../6.3%20Keyboard%20and%20Focus/README.md)

- [Правило первого шага](#правило-первого-шага)
- [Частые атрибуты](#частые-атрибуты)
- [Примеры](#примеры)
- [Live regions](#live-regions)
- [Чего избегать](#чего-избегать)
- [Дальше](#дальше)

Подробнее: [MDN: ARIA](https://developer.mozilla.org/ru/docs/Web/Accessibility/ARIA).

## Правило первого шага

**Сначала нативный HTML**, ARIA — когда его недостаточно:

| Задача | Правильно | Плохо |
|--------|-----------|-------|
| Кнопка | `<button>` | `<div role="button">` |
| Ссылка | `<a href="…">` | `<span role="link">` |
| Поле ввода | `<input>` + `<label>` | `aria-label` без label |
| Заголовок | `<h2>` | `<div role="heading" aria-level="2">` |

Дублировать семантику тега ARIA не нужно: `<button role="button">` — лишнее.

## Частые атрибуты

| Атрибут | Назначение |
|---------|------------|
| `aria-label` | Имя элемента, если нет видимого текста (icon-only кнопка) |
| `aria-labelledby` | `id` элемента-заголовка |
| `aria-describedby` | `id` подсказки или ошибки |
| `aria-expanded` | Раскрыт ли блок (`true` / `false`) |
| `aria-hidden="true"` | Скрыть декоративный элемент от скринридера |
| `aria-live` | Область с динамически обновляемым текстом |
| `aria-current` | Текущий пункт (`page`, `step`, `true`) |

## Примеры

**Кнопка только с иконкой:**

```html
<button type="button" aria-label="Закрыть">
    <svg aria-hidden="true">…</svg>
</button>
```

**Навигация с подписью:**

```html
<nav aria-label="Главное меню">…</nav>
```

**Раскрывающееся меню (кастомный виджет):**

```html
<button aria-expanded="false" aria-controls="submenu" id="menu-btn">
    Продукты
</button>
<ul id="submenu" hidden>…</ul>
```

При открытии меняйте `aria-expanded` на `true` и снимайте `hidden` — в JS.

**Ошибка формы:**

```html
<input id="email" aria-describedby="email-error" aria-invalid="true">
<p id="email-error">Введите корректный email</p>
```

## Live regions

Для сообщений, которые появляются без перезагрузки (уведомления, счётчик, статус поиска):

```html
<div aria-live="polite" id="status"></div>
```

| Значение | Поведение |
|----------|-----------|
| `polite` | Объявит, когда пользователь закончит текущее действие |
| `assertive` | Прервёт и объявит сразу (ошибки, критичные алерты) |
| `off` | Не объявлять (по умолчанию) |

Не злоупотребляйте `assertive` — раздражает при частых обновлениях.

## Чего избегать

- `aria-hidden="true"` на интерактивном контенте — элемент станет недоступен
- `tabindex` больше 0 — ломает естественный порядок Tab
- ARIA вместо `<label>` у полей форм
- Пустой `aria-label` на видимой кнопке с текстом

Нативные [`<dialog>`](../../2.%20Basic%20HTML/2.34%20HTML%20Dialog/README.md) и [`popover`](../../2.%20Basic%20HTML/2.36%20HTML%20Popover/README.md) уже решают часть задач фокуса и модальности.

## Дальше

- [Изображения и медиа](../6.5%20Images%20and%20Media/README.md)
- [Практика: аудит](../6.6%20Accessibility%20Audit/README.md)
- [Формы](../../3.%20HTML%20Forms/README.md)
- [Dialog](../../2.%20Basic%20HTML/2.34%20HTML%20Dialog/README.md)
