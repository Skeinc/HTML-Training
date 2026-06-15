# Основы HTML-форм

Форма собирает ввод пользователя и отправляет его на сервер (или обрабатывает на клиенте через JS).

← [HTML Forms](../README.md) · [Атрибуты form](../3.2%20HTML%20Form%20Attributes/README.md) · [Элементы](../3.3%20HTML%20Form%20Elements/README.md)

- [Контейнер `<form>`](#контейнер-form)
- [`<input>` и `name`](#input-и-name)
- [`<label>`](#label)
- [Radio и checkbox](#radio-и-checkbox)
- [Отправка](#отправка)
- [Дальше](#дальше)

## Контейнер `<form>`

```html
<form action="/search" method="get">
    <!-- поля ввода -->
    <button type="submit">Найти</button>
</form>
```

| Атрибут | Назначение |
|---------|------------|
| `action` | URL обработчика (куда уйдут данные) |
| `method` | `get` или `post` — см. [атрибуты form](../3.2%20HTML%20Form%20Attributes/README.md) |

Без `action` отправка идёт на текущий URL.

## `<input>` и `name`

`<input>` — основной элемент ввода. Вид зависит от `type` (по умолчанию `text`).

```html
<label for="email">Email:</label>
<input type="email" id="email" name="email">
```

**`name` обязателен для отправки:** без него значение поля не попадёт в запрос.

```html
<!-- уйдёт: ?email=user%40mail.ru -->
<input type="email" name="email" value="user@mail.ru">
```

`id` связывает поле с `<label>` и нужен для JS — не путать с `name`.

## `<label>`

```html
<label for="phone">Телефон:</label>
<input type="tel" id="phone" name="phone">
```

- Скринридер озвучивает подпись при фокусе
- Клик по тексту label фокусирует/переключает связанное поле
- `for` на label = `id` на input

Альтернатива — обернуть input внутрь label:

```html
<label>
    <input type="checkbox" name="agree" value="yes">
    Согласен с условиями
</label>
```

## Radio и checkbox

**Radio** — один вариант из группы (общий `name`):

```html
<fieldset>
    <legend>Любимый язык</legend>
    <label><input type="radio" name="lang" value="html"> HTML</label>
    <label><input type="radio" name="lang" value="css"> CSS</label>
    <label><input type="radio" name="lang" value="js"> JavaScript</label>
</fieldset>
```

**Checkbox** — ноль или несколько вариантов:

```html
<label><input type="checkbox" name="notify" value="email"> Email</label>
<label><input type="checkbox" name="notify" value="sms"> SMS</label>
```

## Отправка

```html
<button type="submit">Отправить</button>
<!-- или -->
<input type="submit" value="Отправить">
```

`<button type="button">` — обычная кнопка без отправки формы.

Полный пример — в [`index.html`](index.html).

## Дальше

- [Атрибуты `<form>`](../3.2%20HTML%20Form%20Attributes/README.md)
- [Типы input](../3.4%20HTML%20Input%20Types/README.md)
- [Атрибуты input](../3.5%20HTML%20Input%20Attributes/README.md)
