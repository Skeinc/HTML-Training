# HTML — шпаргалка

Краткая сводка по всей серии. Подробности — в разделах ниже.

← [HTML Training](README.md)

---

## Документ

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Заголовок — Бренд</title>
</head>
<body>…</body>
</html>
```

| | HTML | CSS | JS |
|---|------|-----|-----|
| Задача | Структура, смысл | Оформление | Поведение |

---

## Частые ошибки (из квизов)

| Ошибка | Правильно |
|--------|-----------|
| `<!--` без `!` | `<!-- комментарий -->` |
| Якорь `href="/"` | `href="#id"` + `id` на элементе |
| `&lt;` не знаю | `&lt;` → символ `<` на экране |
| Два `h1`, пропуск `h2` | Один `h1`, иерархия без пропусков |
| `disabled` не отправляется | `readonly` отправляется |
| `novalidate` на одну кнопку | `formnovalidate` на кнопке |
| Пароль через GET | `method="post"` + HTTPS |
| `aria-label` на иконке | `aria-label` на **кнопке**, иконка `aria-hidden` |
| Декоративный `alt="разделитель"` | `alt=""` |
| POUR: клавиатура = P | Клавиатура = **O (Operable)** |

---

## Текст и разметка

| Тема | Запомнить |
|------|-----------|
| Заголовки | `h1`–`h6`, один `h1`, без пропусков |
| Смысл | `strong` / `em`, не только `b` / `i` |
| Цитаты | `blockquote` (блок), `q` (в строке) |
| Код в тексте | `&lt;p&gt;`, не голый `<` |
| Сущности | `&lt;` `&gt;` `&amp;` = тот же символ, другая запись |

**Семантика:** `header`, `nav`, `main`, `article`, `section`, `footer` — не только `div`.

---

## Ссылки, изображения, пути

```html
<a href="https://site.com" target="_blank" rel="noopener noreferrer">Сайт</a>
<a href="#contacts">К разделу</a>

<img src="photo.jpg" alt="Описание" width="400" height="300" loading="lazy">
```

| | |
|---|---|
| `srcset` / `sizes` | Браузер выбирает файл (retina, ширина) |
| `<picture>` | Разные форматы (WebP) + media |
| `alt=""` | Только декоративные картинки |
| `./` / `../` | Текущая папка / уровень выше |

`width`/`height` в HTML — резерв места (CLS), даже если размер в CSS.

---

## CSS в HTML

| Способ | Когда |
|--------|-------|
| `<link rel="stylesheet">` | Проекты (лучший) |
| `<style>` в `<head>` | Страница целиком |
| `style="…"` | Прототип, одноразово |

---

## Формы

```html
<form action="/save" method="post" enctype="multipart/form-data">
    <label for="email">Email</label>
    <input type="email" id="email" name="email" required>
    <button type="submit">Отправить</button>
</form>
```

| | GET | POST |
|---|-----|------|
| Данные | В URL `?q=…` | В теле запроса |
| Когда | Поиск, фильтры | Логин, файлы, личные данные |

| Атрибут | Назначение |
|---------|------------|
| `name` | Обязателен для отправки (≠ `id`) |
| `enctype="multipart/form-data"` | Загрузка файлов |
| `readonly` | Отправляется |
| `disabled` | Не отправляется |
| `formaction` | Другой URL у кнопки submit |
| `formnovalidate` | Submit без валидации (одна кнопка) |

Radio — общий `name`; checkbox — несколько значений.

---

## Graphics

| | Canvas | SVG | `<img>` |
|---|--------|-----|---------|
| Тип | Растр + JS | Вектор в XML | Фото |
| DOM фигур | Нет | Да | — |
| Когда | Игры, частая перерисовка | Иконки, диаграммы | Фото |

Canvas: `getContext('2d')`, анимация — `requestAnimationFrame`.

---

## Media

```html
<video controls poster="preview.jpg">
    <source src="clip.webm" type="video/webm">
    <source src="clip.mp4" type="video/mp4">
    <track kind="subtitles" src="ru.vtt" srclang="ru" label="Русский">
</video>
```

| | |
|---|---|
| Свой файл | `<video>` / `<audio>` |
| YouTube | `<iframe src="https://www.youtube.com/embed/ID">` |
| Фон без звука | `autoplay muted loop playsinline` |
| `captions` | Речь + звуки (глухие) |
| `subtitles` | Перевод речи |

---

## Доступность (a11y)

**POUR:** Perceivable · **Operable** · Understandable · Robust

```html
<a href="#main" class="skip-link">Перейти к содержимому</a>
<main id="main">…</main>

<button type="button" aria-label="Закрыть">
    <svg aria-hidden="true">…</svg>
</button>
```

| Правило | |
|---------|--|
| Сначала нативный HTML | `<button>`, `<label>`, не `div role="button"` |
| Ошибки форм | Текст + `aria-invalid` + `aria-describedby`, не только цвет |
| Контраст | ≥ 4.5:1 |
| Tab | Вся страница без мыши; `tabindex > 0` — избегать |
| Модалки | `<dialog>` + `showModal()` |

Инструменты: Lighthouse, axe, VoiceOver (Cmd+F5), Tab-прогон.

---

## SEO

```html
<head>
    <title>Уникальный заголовок — Бренд</title>
    <meta name="description" content="150–160 символов, по смыслу">
    <link rel="canonical" href="https://example.com/page">
    <meta name="robots" content="noindex">  <!-- если не для поиска -->
</head>
```

| | |
|---|---|
| `meta keywords` | Игнорируются |
| `canonical` | Одна URL при дублях (`?utm_…`) |
| `noindex` | Сильнее `Disallow` для выдачи |
| `robots.txt` | Рекомендация, не защита |
| `sitemap.xml` | Список URL для краулера |
| `hreflang` | Мультиязычные версии |

**Open Graph:** `og:title`, `og:image` (абсолютный `https://…`), `og:url`.

**JSON-LD:** `<script type="application/ld+json">` — только то, что видно на странице.

**Core Web Vitals:**

| Метрика | Что | Норма |
|---------|-----|-------|
| LCP | Главный контент виден | ≤ 2.5 с |
| INP | Отклик на действия | ≤ 200 мс |
| CLS | Скачок вёрстки | ≤ 0.1 |

HTML: `width`/`height` на img/video, `defer` на скриптах, `lazy` не на hero.

---

## Современный HTML

| Тег / атрибут | Назначение |
|---------------|------------|
| `<dialog>` | Модалка, `showModal()`, Esc |
| `popover` | Всплывашка без блокировки страницы |
| `<progress>` | Процесс (загрузка) |
| `<meter>` | Показатель (диск, рейтинг) |

---

## Чеклист готовой страницы

- [ ] `<!DOCTYPE html>`, `lang`, `charset`, `viewport`
- [ ] Один `h1`, логичные подзаголовки
- [ ] У форм — `label`, у img — `alt`
- [ ] Формы с личными данными — POST + HTTPS
- [ ] `canonical`, `title`, `description`
- [ ] Страница проходима с Tab, виден фокус
- [ ] Нет `user-scalable=no`

---

## Куда дальше

- [CSS-Training](../CSS-Training/README.md)
- [Интернет](../Internet/README.md) — HTTP, URL, DNS
- [HTML Reference](HTML%20Reference/README.md) — все теги
