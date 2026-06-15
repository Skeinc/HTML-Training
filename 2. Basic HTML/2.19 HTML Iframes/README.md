# iframe в HTML

Встраивание одной HTML-страницы внутрь другой.

← [Базовый HTML](../README.md)

- [Синтаксис](#синтаксис)
- [Атрибуты](#атрибуты)
- [Безопасность](#безопасность)
- [Альтернативы](#альтернативы)

## Синтаксис

```html
<iframe
    src="https://example.com/embed"
    title="Встроенная карта"
    width="100%"
    height="400"
    loading="lazy"
></iframe>
```

`title` **обязателен** для доступности — скринридеры озвучивают его.

## Атрибуты

| Атрибут | Назначение |
|---------|------------|
| `src` | URL встраиваемой страницы |
| `name` | Имя фрейма — цель для `target` у ссылки |
| `sandbox` | Ограничения для встроенного контента |
| `allow` | Разрешения (камера, геолокация…) |

Ссылка открывается **внутри** iframe:

```html
<iframe name="preview" src="about:blank" title="Превью"></iframe>
<a href="page.html" target="preview">Открыть в превью</a>
```

Граница убирается через CSS: `border: none;` (атрибут `frameborder` устарел).

## Безопасность

- Встраивайте только **доверенные** источники
- `sandbox` без флагов блокирует скрипты, формы, same-origin
- Для `target="_blank"` у ссылок используйте `rel="noopener noreferrer"` — см. [Ссылки](../2.9%20HTML%20Links/README.md)

```html
<iframe sandbox="allow-scripts allow-same-origin" …></iframe>
```

Сторонние виджеты (YouTube, карты) обычно дают готовый embed-код.

## Альтернативы

| Задача | Лучше чем iframe |
|--------|------------------|
| Видео | `<video>`, `<iframe>` от провайдера |
| Весь layout сайта | семантическая разметка + CSS |
| Данные с API | fetch + JS |

## Дальше

- [HTML Media](../../5.%20HTML%20Media/README.md)
