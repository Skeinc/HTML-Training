# Диалоговые окна (`<dialog>`)

Нативное модальное окно без сторонних библиотек. Браузер даёт фокус, закрытие по Esc и затемнение фона.

← [Базовый HTML](../README.md) · [Семантика](../2.26%20HTML%20Semantics/README.md) · [Popover](../2.36%20HTML%20Popover/README.md)

- [Разметка](#разметка)
- [Открытие и закрытие](#открытие-и-закрытие)
- [Доступность](#доступность)
- [Дальше](#дальше)

## Разметка

```html
<dialog id="confirm">
    <h2>Удалить файл?</h2>
    <p>Действие необратимо.</p>
    <form method="dialog">
        <button value="cancel">Отмена</button>
        <button value="ok">Удалить</button>
    </form>
</dialog>
<button type="button" id="open">Удалить</button>
```

| Атрибут | Назначение |
|---------|------------|
| `open` | Диалог виден сразу (для демо; в проде открывают через JS) |

По умолчанию `<dialog>` скрыт. Атрибут `open` без JS — только для статичных примеров.

## Открытие и закрытие

```javascript
const dialog = document.getElementById('confirm');
const openBtn = document.getElementById('open');

openBtn.addEventListener('click', () => dialog.showModal());
// dialog.show() — без модального фона

dialog.addEventListener('close', () => {
    console.log('Результат:', dialog.returnValue); // "ok" | "cancel"
});
```

| Метод | Поведение |
|-------|-----------|
| `showModal()` | Модально: фокус внутри, фон неактивен, Esc закрывает |
| `show()` | Обычное окно без блокировки страницы |
| `close(returnValue?)` | Закрыть; `returnValue` — строка для обработчика `close` |

Кнопка с `method="dialog"` внутри `<form>` закрывает диалог; `value` попадает в `returnValue`.

## Доступность

- `showModal()` переносит фокус в диалог и ловит Tab внутри
- Заголовок (`<h2>`) описывает суть действия
- Для простых подсказок без блокировки страницы смотрите [Popover](../2.36%20HTML%20Popover/README.md)
- Подробнее про ARIA — [6.2 ARIA](../../6.%20HTML%20Accessibillity/6.2%20HTML%20ARIA/README.md)

Пример — в [`index.html`](index.html).

## Дальше

- [Popover](../2.36%20HTML%20Popover/README.md)
- [JavaScript](../2.20%20HTML%20JavaScript/README.md)
- [Основы доступности](../../6.%20HTML%20Accessibillity/6.1%20HTML%20Accessibility%20Basics/README.md)
