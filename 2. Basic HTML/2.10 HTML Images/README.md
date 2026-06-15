# Изображения в HTML

Тег `<img>` встраивает картинку по URL. Обязателен осмысленный `alt`.

← [Базовый HTML](../README.md) · [Ссылки](../2.9%20HTML%20Links/README.md) · [Пути](../2.21%20HTML%20File%20Paths/README.md)

- [Основы](#основы)
- [Размер и адаптивность](#размер-и-адаптивность)
- [`srcset` и `sizes`](#srcset-и-sizes)
- [`picture`](#picture)
- [Дополнительно](#дополнительно)
- [Дальше](#дальше)

## Основы

```html
<img src="photo.jpg" alt="Осенние листья на дорожке">
```

| Атрибут | Назначение |
|---------|------------|
| `src` | Путь или URL изображения |
| `alt` | Текстовое описание (для a11y и если картинка не загрузилась) |
| `width` / `height` | Размер в пикселях — снижает скачок layout при загрузке |
| `loading="lazy"` | Отложенная загрузка при прокрутке |

`alt=""` допустим только для **декоративных** изображений.

**Ссылка-картинка:**

```html
<a href="gallery.html">
    <img src="thumb.jpg" alt="Открыть галерею">
</a>
```

## Размер и адаптивность

```html
<!-- фиксированный размер -->
<img src="photo.jpg" alt="…" width="400" height="300">

<!-- адаптивно через CSS (предпочтительно) -->
<img src="photo.jpg" alt="…" style="max-width: 100%; height: auto;">
```

Внешние изображения (`src` с чужого домена) могут исчезнуть или нарушать авторские права — хостите важный контент сами.

## `srcset` и `sizes`

Браузер сам выбирает файл под плотность пикселей и ширину экрана — без `<picture>`.

**Retina / разная плотность экрана:**

```html
<img
    src="photo.jpg"
    srcset="photo.jpg 1x, photo-2x.jpg 2x"
    alt="Пейзаж">
```

**Несколько ширин + подсказка браузеру:**

```html
<img
    src="photo-800.jpg"
    srcset="photo-400.jpg 400w, photo-800.jpg 800w, photo-1200.jpg 1200w"
    sizes="(max-width: 600px) 100vw, 50vw"
    alt="Пейзаж">
```

| Атрибут | Назначение |
|---------|------------|
| `srcset` | Список URL с дескрипторами `400w` (ширина) или `2x` (плотность) |
| `sizes` | Какую ширину займёт картинка в layout — браузер выберет лучший файл из `srcset` |
| `src` | Fallback, если `srcset` не поддерживается |

`src` должен указывать на разумный вариант по умолчанию (часто средний по размеру).

## `picture`

Разные файлы под размер экрана или формат:

```html
<picture>
    <source media="(max-width: 600px)" srcset="photo-small.jpg">
    <source srcset="photo.webp" type="image/webp">
    <img src="photo.jpg" alt="Описание">
</picture>
```

`<img>` в конце — fallback для старых браузеров.

## Дополнительно

| Тема | Кратко |
|------|--------|
| Форматы | JPEG (фото), PNG (прозрачность), WebP/AVIF (современные), SVG (вектор), GIF/APNG (анимация) |
| `<figure>` + `<figcaption>` | Изображение с подписью |
| `<map>` + `<area>` | Кликабельные зоны (редко; лучше SVG/CSS) |
| Фон | `background-image` в CSS, не `<img>` |

SVG inline — в [HTML Graphics](../../4.%20HTML%20Graphics/4.2%20HTML%20SVG/README.md).

## Дальше

- [Адаптивность](../2.24%20HTML%20Responsive/README.md)
- [Основы доступности](../../6.%20HTML%20Accessibillity/6.1%20HTML%20Accessibility%20Basics/README.md)
