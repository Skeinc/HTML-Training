# HTTP-коды ответа (кратко)

Трёхзначный код в ответе сервера: успех, редирект или ошибка.

← [HTML Reference](../README.md)

**Подробно:** [Интернет: HTTP](../../Internet/2.%20What%20is%20HTTP%3F/README.md)

| Код | Группа | Примеры |
|-----|--------|---------|
| **1xx** | Информация | 100 Continue |
| **2xx** | Успех | **200** OK, **201** Created, **204** No Content |
| **3xx** | Редирект | **301** Moved Permanently, **302** Found, **304** Not Modified |
| **4xx** | Ошибка клиента | **400** Bad Request, **401** Unauthorized, **403** Forbidden, **404** Not Found |
| **5xx** | Ошибка сервера | **500** Internal Server Error, **502** Bad Gateway, **503** Service Unavailable |

В браузере при навигации вы видите страницу тела ответа (HTML для 404) или редирект (3xx).

[MDN: HTTP response status codes](https://developer.mozilla.org/ru/docs/Web/HTTP/Reference/Status)
