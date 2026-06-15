# Элементы HTML-форм

Помимо `<input>` — выпадающие списки, многострочный текст, группировка и подсказки.

← [HTML Forms](../README.md) · [Основы](../3.1%20HTML%20Forms/README.md) · [Типы input](../3.4%20HTML%20Input%20Types/README.md)

- [select и option](#select-и-option)
- [textarea](#textarea)
- [button](#button)
- [fieldset и legend](#fieldset-и-legend)
- [datalist](#datalist)
- [output](#output)
- [Дальше](#дальше)

## select и option

```html
<label for="city">Город:</label>
<select id="city" name="city">
    <option value="">— выберите —</option>
    <option value="msk" selected>Москва</option>
    <option value="spb">Санкт-Петербург</option>
</select>
```

| Атрибут | Назначение |
|---------|------------|
| `multiple` | Несколько значений (с Ctrl/Cmd) |
| `size` | Число видимых строк |
| `selected` на `<option>` | Значение по умолчанию |

Группировка — `<optgroup label="…">`.

## textarea

Многострочный ввод:

```html
<label for="msg">Сообщение:</label>
<textarea id="msg" name="msg" rows="5" cols="40"
    placeholder="Ваш текст…"></textarea>
```

Размер лучше задавать в CSS (`width`, `min-height`), не только `cols`/`rows`.

## button

```html
<button type="submit">Отправить</button>
<button type="reset">Сбросить</button>
<button type="button">Действие (JS)</button>
```

**Всегда указывайте `type`.** Без него в некоторых браузерах `<button>` внутри формы ведёт себя как submit.

`<input type="submit">` — альтернатива, но внутри `<button>` можно вложить HTML (иконку).

## fieldset и legend

Группировка связанных полей (особенно radio/checkbox):

```html
<fieldset>
    <legend>Контактные данные</legend>
    <label>Имя <input type="text" name="fname"></label>
    <label>Фамилия <input type="text" name="lname"></label>
</fieldset>
```

`disabled` на `<fieldset>` отключает все поля внутри.

## datalist

Подсказки при вводе (не строгий список, как у `select`):

```html
<label for="browser">Браузер:</label>
<input list="browsers" id="browser" name="browser">
<datalist id="browsers">
    <option value="Chrome">
    <option value="Firefox">
    <option value="Safari">
</datalist>
```

`list` на input = `id` на datalist.

## output

Результат вычисления (часто с JS):

```html
<form oninput="result.value = parseInt(a.value) + parseInt(b.value)">
    <input type="range" id="a" name="a" value="50"> +
    <input type="range" id="b" name="b" value="50"> =
    <output name="result" for="a b">100</output>
</form>
```

Для продакшена предпочтительнее обработчик в JS-файле, не `oninput` в HTML.

## Дальше

- [Типы input](../3.4%20HTML%20Input%20Types/README.md)
- [Атрибут list](../3.5%20HTML%20Input%20Attributes/README.md)
