# Формы и сообщения об ошибках

Поле формы должно быть понятно **до** ввода, при ошибке — **не только красной рамкой**.

← [Доступность](../README.md) · [Клавиатура](../6.3%20Keyboard%20and%20Focus/README.md) · [Изображения](../6.5%20Images%20and%20Media/README.md)

- [Минимум](#минимум)
- [Ошибки в HTML](#ошибки-в-html)
- [Не только цветом](#не-только-цветом)
- [Группы полей](#группы-полей)
- [Дальше](#дальше)

## Минимум

```html
<label for="email">Email</label>
<input type="email" id="email" name="email" required autocomplete="email">
```

| Правило | Зачем |
|---------|-------|
| `<label for="id">` | Скринридер озвучивает подпись; клик по label фокусирует поле |
| `required`, `type` | Встроенная проверка браузера |
| `autocomplete` | Помогает автозаполнению |

`placeholder` **не заменяет** label — подсказка исчезает при вводе.

## Ошибки в HTML

```html
<label for="email">Email</label>
<input type="email" id="email" name="email" required
    aria-invalid="true"
    aria-describedby="email-error">
<p id="email-error" role="alert">Введите адрес в формате name@example.com</p>
```

| Атрибут | Назначение |
|---------|------------|
| `aria-invalid="true"` | Поле с ошибкой |
| `aria-describedby` | Связь с текстом ошибки или подсказки |
| `role="alert"` | Скринридер объявит сообщение сразу |

После исправления снимайте `aria-invalid` и обновляйте текст ошибки в JS.

## Не только цветом

Плохо: красная рамка без текста.

Хорошо: текст + иконка + цвет:

```html
<p id="email-error">
    <span aria-hidden="true">⚠</span>
    Введите корректный email
</p>
```

Контраст текста ошибки с фоном — не ниже 4.5:1.

## Группы полей

Radio и checkbox — в `<fieldset>` с `<legend>`:

```html
<fieldset>
    <legend>Способ доставки</legend>
    <label><input type="radio" name="ship" value="pickup"> Самовывоз</label>
    <label><input type="radio" name="ship" value="courier"> Курьер</label>
</fieldset>
```

`disabled` на `<fieldset>` отключает все поля внутри.

Пример — в [`index.html`](index.html).

## Дальше

- [ARIA](../6.2%20HTML%20ARIA/README.md)
- [Атрибуты input](../../3.%20HTML%20Forms/3.5%20HTML%20Input%20Attributes/README.md)
