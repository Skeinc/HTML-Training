# Атрибуты `form*` у `<input>`

Связь поля или кнопки submit с формой и переопределение параметров отправки.

← [HTML Forms](../README.md) · [Атрибуты form](../3.2%20HTML%20Form%20Attributes/README.md) · [Атрибуты input](../3.5%20HTML%20Input%20Attributes/README.md)

- [form](#form)
- [formaction, formmethod, formenctype, formtarget](#formaction-formmethod-formenctype-formtarget)
- [formnovalidate](#formnovalidate)
- [Когда нужно](#когда-нужно)

Работают в основном с `type="submit"` и `type="image"`, кроме `form`.

## form

Поле **вне** тега `<form>`, но участвует в его отправке:

```html
<form id="profile-form" action="/save" method="post">
    <input name="name" required>
    <button type="submit">Сохранить</button>
</form>

<label for="bio">О себе (вне формы):</label>
<textarea id="bio" name="bio" form="profile-form"></textarea>
```

`form` на input = `id` на `<form>`.

## formaction, formmethod, formenctype, formtarget

Переопределяют атрибуты `<form>` **для конкретной кнопки** submit:

```html
<form action="/default" method="post">
    <input name="title" required>

    <button type="submit">Обычная отправка</button>
    <button type="submit" formaction="/draft" formmethod="post">
        Сохранить черновик
    </button>
    <button type="submit" formaction="/preview" formtarget="_blank">
        Предпросмотр
    </button>
</form>
```

| Атрибут | Переопределяет |
|---------|----------------|
| `formaction` | `action` |
| `formmethod` | `method` (`get` / `post`) |
| `formenctype` | `enctype` (например `multipart/form-data`) |
| `formtarget` | `target` (`_blank` и др.) |

## formnovalidate

Отправить **без** HTML5-валидации этой кнопкой:

```html
<form>
    <input type="email" name="email" required>
    <button type="submit">Отправить</button>
    <button type="submit" formnovalidate>Сохранить без проверки</button>
</form>
```

Переопределяет `novalidate` на форме для одной кнопки.

## Когда нужно

| Сценарий | Атрибут |
|----------|---------|
| Поле визуально вне `<form>` (сложная вёрстка) | `form` |
| «Сохранить» vs «Опубликовать» на разные URL | `formaction` |
| Черновик без строгой валидации | `formnovalidate` |
| Открыть результат в новой вкладке | `formtarget="_blank"` |

В большинстве форм достаточно одной кнопки и атрибутов на `<form>`.

## Дальше

- [Атрибуты `<form>`](../3.2%20HTML%20Form%20Attributes/README.md)
- [HTTP](../../Internet/2.%20What%20is%20HTTP%3F/README.md)
