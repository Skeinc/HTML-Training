# Типы `<input>`

Атрибут `type` меняет вид поля, клавиатуру на мобильных и встроенную валидацию.

← [HTML Forms](../README.md) · [Основы](../3.1%20HTML%20Forms/README.md) · [Атрибуты input](../3.5%20HTML%20Input%20Attributes/README.md)

- [Текст и данные](#текст-и-данные)
- [Выбор](#выбор)
- [Кнопки](#кнопки)
- [Дата и время](#дата-и-время)
- [Файлы и скрытые](#файлы-и-скрытые)
- [Дальше](#дальше)

По умолчанию `type="text"`.

## Текст и данные

| type | Назначение |
|------|------------|
| `text` | Однострочный текст |
| `password` | Пароль (маскируется) |
| `email` | Email + базовая проверка формата |
| `tel` | Телефон (клавиатура цифр на мобильных) |
| `url` | URL |
| `search` | Поле поиска |
| `number` | Число; с `min`, `max`, `step` |
| `color` | Выбор цвета |

```html
<input type="email" name="email" required>
<input type="number" name="qty" min="1" max="99" value="1">
<input type="tel" name="phone" pattern="\+7[0-9]{10}">
```

## Выбор

| type | Назначение |
|------|------------|
| `checkbox` | Флажок (несколько из многих) |
| `radio` | Переключатель (один из группы с общим `name`) |
| `range` | Ползунок (`min`, `max`, `step`) |

```html
<input type="range" name="volume" min="0" max="100" value="50">
```

## Кнопки

| type | Назначение |
|------|------------|
| `submit` | Отправить форму |
| `reset` | Сбросить к начальным значениям |
| `button` | Обычная кнопка (JS) |
| `image` | Картинка как submit (`src`, `alt`) |

Предпочитайте `<button type="submit">` для гибкой вёрстки.

## Дата и время

| type | Значение |
|------|----------|
| `date` | Дата |
| `time` | Время |
| `datetime-local` | Дата + время (без часового пояса) |
| `month` | Месяц и год |
| `week` | Неделя и год |

```html
<input type="date" name="birth" max="2010-12-31">
<input type="time" name="meeting">
```

Виджет зависит от браузера; формат значения — ISO-подобный (`YYYY-MM-DD`).

## Файлы и скрытые

| type | Назначение |
|------|------------|
| `file` | Загрузка файла; `multiple`, `accept` |
| `hidden` | Скрытое поле (id записи, токен) — **не** защита |

```html
<input type="file" name="doc" accept=".pdf,image/*" multiple>
<input type="hidden" name="order_id" value="42">
```

`hidden` видно в DevTools — не храните там секреты.

## Дальше

- [Атрибуты input](../3.5%20HTML%20Input%20Attributes/README.md) — `required`, `placeholder`, `pattern`
- [enctype](../3.2%20HTML%20Form%20Attributes/README.md) — для `file`
