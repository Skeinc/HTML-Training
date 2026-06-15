# Атрибуты `<form>`

Куда, как и в каком виде отправляются данные формы.

← [HTML Forms](../README.md) · [Основы](../3.1%20HTML%20Forms/README.md) · [Элементы](../3.3%20HTML%20Form%20Elements/README.md)

- [action и method](#action-и-method)
- [GET vs POST](#get-vs-post)
- [enctype](#enctype)
- [Прочие атрибуты](#прочие-атрибуты)
- [Дальше](#дальше)

Подробнее о HTTP — [Интернет: HTTP](../../Internet/2.%20What%20is%20HTTP%3F/README.md).

## action и method

```html
<form action="/api/login" method="post">
    …
</form>
```

| Атрибут | Назначение |
|---------|------------|
| `action` | URL обработчика |
| `method` | `get` (по умолчанию) или `post` |
| `target` | Где показать ответ: `_self`, `_blank`, имя iframe |

## GET vs POST

| | GET | POST |
|---|-----|------|
| Данные | В URL (`?name=value&…`) | В теле запроса |
| Закладки | Можно | Нельзя |
| Размер | Ограничен (~2 KB URL) | Большие формы, файлы |
| Конфиденциальность | Видно в адресной строке | Не в URL (но не шифрование!) |
| Когда | Поиск, фильтры | Логин, регистрация, загрузка файлов |

**Пароли и личные данные** — только POST (+ HTTPS). GET для поиска: `/search?q=html`.

## enctype

Как кодировать тело запроса при `method="post"`:

| Значение | Когда |
|----------|-------|
| `application/x-www-form-urlencoded` | По умолчанию, обычные поля |
| `multipart/form-data` | Загрузка файлов (`<input type="file">`) |
| `text/plain` | Редко |

```html
<form action="/upload" method="post" enctype="multipart/form-data">
    <input type="file" name="avatar">
</form>
```

## Прочие атрибуты

| Атрибут | Назначение |
|---------|------------|
| `autocomplete="on\|off"` | Подсказки браузера из прошлых вводов |
| `novalidate` | Отключить встроенную HTML5-валидацию при submit |
| `name` | Имя формы (для `document.forms`, атрибут `form` у input) |

```html
<form action="/register" method="post" autocomplete="on" novalidate>
```

`novalidate` не отменяет проверку на сервере — она обязательна.

## Дальше

- [Атрибуты `form*` у input](../3.6%20HTML%20Input%20form%20Attributes/README.md) — разные кнопки submit
- [Валидация](../3.5%20HTML%20Input%20Attributes/README.md) — `required`, `pattern`
