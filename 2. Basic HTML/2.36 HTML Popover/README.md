# Popover (атрибут `popover`)

Всплывающий блок без JavaScript-библиотек: подсказки, меню, панели. Легче `<dialog>`, если не нужна жёсткая модальность.

← [Базовый HTML](../README.md) · [Dialog](../2.34%20HTML%20Dialog/README.md)

- [Разметка](#разметка)
- [Управление](#управление)
- [Когда что выбрать](#когда-что-выбрать)
- [Дальше](#дальше)

## Разметка

```html
<button type="button" popovertarget="hint">Подсказка</button>
<div id="hint" popover>Текст подсказки появится здесь.</div>
```

| Атрибут | Где | Назначение |
|---------|-----|------------|
| `popover` | всплывающий элемент | Включает режим popover |
| `popover="auto"` | то же | Закрывается при клике снаружи (по умолчанию) |
| `popover="manual"` | то же | Только явное закрытие |
| `popovertarget` | кнопка | `id` popover-элемента для toggle |
| `popovertargetaction` | кнопка | `toggle` (по умолчанию), `show`, `hide` |

```html
<button popovertarget="menu" popovertargetaction="show">Открыть</button>
<button popovertarget="menu" popovertargetaction="hide">Закрыть</button>
<nav id="menu" popover>
    <a href="/">Главная</a>
    <a href="/about">О нас</a>
</nav>
```

## Управление

Через JavaScript — те же методы, что у dialog:

```javascript
const hint = document.getElementById('hint');
hint.showPopover();
hint.hidePopover();
hint.togglePopover();
```

События: `beforetoggle`, `toggle` — удобно для аналитики и фокуса.

## Когда что выбрать

| Задача | Решение |
|--------|---------|
| Подтверждение удаления, блокировка фона | [`<dialog>`](../2.34%20HTML%20Dialog/README.md) + `showModal()` |
| Подсказка, выпадающее меню | `popover` |
| Раскрывающийся блок в потоке страницы | `<details>` / `<summary>` — [Семантика](../2.26%20HTML%20Semantics/README.md) |

Пример — в [`index.html`](index.html).

## Дальше

- [Dialog](../2.34%20HTML%20Dialog/README.md)
- [Глобальные атрибуты](../../../HTML%20Reference/HTML%20Global%20Attributes/README.md)
