# JavaScript в HTML

Подключение скриптов к странице. Логику пишут в `.js`, в HTML — только подключение.

← [Базовый HTML](../README.md) · [Head](../2.22%20HTML%20Head/README.md)

- [Способы подключения](#способы-подключения)
- [Где размещать](#где-размещать)
- [`noscript`](#noscript)
- [Практика](#практика)

## Способы подключения

**Внешний файл (предпочтительно):**

```html
<script src="app.js" defer></script>
```

**Встроенный код:**

```html
<script>
    console.log('Привет');
</script>
```

**Обработчики в атрибутах** (`onclick="…"`) — допустимы в учебных примерах; в проектах лучше `addEventListener` в JS-файле.

## Где размещать

| Вариант | Плюсы |
|---------|-------|
| `<script defer src="…">` в `<head>` | Не блокирует парсинг; выполнится после разбора DOM |
| `<script src="…">` перед `</body>` | Классический вариант без `defer` |
| `type="module"` | ES-модули, автоматический strict mode |

```html
<head>
    <script src="app.js" defer></script>
</head>
```

Без `defer`/`async` скрипт в `<head>` блокирует отрисовку страницы.

## `noscript`

Контент для пользователей без JavaScript:

```html
<noscript>
    <p>Для работы приложения включите JavaScript.</p>
</noscript>
```

## Практика

- Один файл — одна ответственность; не смешивайте всю логику в HTML
- Доступ к элементам: `document.getElementById()`, `querySelector()`
- Подробнее о языке — вне этой серии (документация MDN)

## Дальше

- [Head](../2.22%20HTML%20Head/README.md)
- [Классы и id](../2.17%20HTML%20Classes/README.md)
