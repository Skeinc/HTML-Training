# Core Web Vitals и скорость

Google учитывает **опыт загрузки** страницы. Часть метрик напрямую связана с HTML.

← [SEO Basics](../README.md) · [Meta robots](../7.4%20Meta%20Robots%20and%20Canonical/README.md) · [Основы](../7.1%20SEO%20Basics/README.md)

- [Три метрики](#три-метрики)
- [HTML-приёмы](#html-приёмы)
- [Что ещё влияет](#что-ещё-влияет)
- [Проверка](#проверка)
- [Дальше](#дальше)

См. также: [Кэширование и CDN](../../../Internet/10.%20Caching%20and%20CDN/README.md).

## Три метрики

| Метрика | Что измеряет | Хорошо |
|---------|--------------|--------|
| **LCP** (Largest Contentful Paint) | Когда виден главный контент | ≤ 2.5 с |
| **INP** (Interaction to Next Paint) | Отклик на действия | ≤ 200 мс |
| **CLS** (Cumulative Layout Shift) | «Прыгает» ли вёрстка | ≤ 0.1 |

## HTML-приёмы

**CLS — резерв места под медиа:**

```html
<img src="hero.jpg" alt="…" width="1200" height="630" loading="lazy">
<video width="640" height="360" poster="preview.jpg" …></video>
```

Без `width`/`height` браузер не знает размер до загрузки → скачок вёрстки.

**LCP — не блокировать отрисовку:**

```html
<link rel="stylesheet" href="styles.css">
<script src="app.js" defer></script>
```

Скрипты в `<head>` без `defer`/`async` задерживают показ контента.

**LCP — быстрый главный контент:**

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
```

`loading="lazy"` на картинках **ниже первого экрана** — не на hero-изображении (оно должно грузиться сразу).

## Что ещё влияет

| Фактор | Где настраивается |
|--------|-------------------|
| Сжатие gzip/brotli | Сервер |
| Кэш статики | Заголовки HTTP, CDN |
| Размер изображений | WebP/AVIF, `srcset` |
| Минификация CSS/JS | Сборка проекта |

Это выходит за рамки HTML, но влияет на SEO так же, как `<title>`.

## Проверка

- Chrome DevTools → **Lighthouse** → Performance
- [PageSpeed Insights](https://pagespeed.web.dev/)
- Google Search Console → Core Web Vitals

## Дальше

- [Основы SEO](../7.1%20SEO%20Basics/README.md)
- [Адаптивность](../../2.%20Basic%20HTML/2.24%20HTML%20Responsive/README.md)
