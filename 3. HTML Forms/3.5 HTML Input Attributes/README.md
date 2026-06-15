# Атрибуты `<input>`

Управление значением, ограничениями, доступностью и валидацией полей.

← [HTML Forms](../README.md) · [Типы input](../3.4%20HTML%20Input%20Types/README.md) · [form*](../3.6%20HTML%20Input%20form%20Attributes/README.md)

- [Значение и состояние](#значение-и-состояние)
- [Ограничения](#ограничения)
- [Валидация](#валидация)
- [UX](#ux)
- [Важно](#важно)

## Значение и состояние

| Атрибут | Эффект |
|---------|--------|
| `value` | Начальное значение |
| `checked` | Выбран radio/checkbox при загрузке |
| `readonly` | Только чтение, **отправляется** с формой |
| `disabled` | Неактивно, **не отправляется** |

```html
<input name="code" value="ABC" readonly>
<input name="promo" disabled>
```

## Ограничения

| Атрибут | Для чего |
|---------|----------|
| `size` | Видимая ширина (в символах) для текстовых типов |
| `maxlength` | Макс. число символов |
| `min` / `max` | Числа, даты, range |
| `step` | Шаг для number, range, date… |
| `multiple` | Несколько файлов или email-адресов |

```html
<input type="number" name="age" min="18" max="120" step="1">
<input type="date" name="start" min="2026-01-01">
```

## Валидация

Браузер проверяет **перед** отправкой (если нет `novalidate` на форме):

| Атрибут | Назначение |
|---------|------------|
| `required` | Поле обязательно |
| `pattern` | RegExp (для text, tel, email…) |
| `minlength` | Минимальная длина строки |

```html
<input type="text" name="country" pattern="[A-Za-z]{2}"
    title="Двухбуквенный код страны" required>
```

Типы `email`, `url`, `number` имеют встроенные правила по `type`.

**Серверная валидация обязательна** — клиентскую можно обойти.

## UX

| Атрибут | Назначение |
|---------|------------|
| `placeholder` | Подсказка в пустом поле (не замена `<label>`) |
| `autocomplete` | `on` / `off` или токен (`email`, `name`…) |
| `autofocus` | Фокус при загрузке (один на страницу) |
| `list` | Связь с `<datalist id="…">` |
| `accept` | Допустимые типы файлов |
| `width` / `height` | Для `type="image"` |

```html
<input type="search" name="q" placeholder="Поиск…" autocomplete="off">
```

## Важно

- У каждого отправляемого поля — уникальный в рамках формы `name`
- `placeholder` + `label`: label для a11y, placeholder — пример формата
- `autofocus` может мешать скринридерам — используйте осознанно

## Дальше

- [Атрибуты form*](../3.6%20HTML%20Input%20form%20Attributes/README.md)
- [Основы доступности](../../6.%20HTML%20Accessibillity/6.1%20HTML%20Accessibility%20Basics/README.md)
