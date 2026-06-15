# HTTP-методы (кратко)

Метод указывает **действие** над ресурсом. В HTML-формах — атрибут `method` на `<form>`.

← [HTML Reference](../README.md)

**Подробно:** [Интернет: HTTP](../../Internet/2.%20What%20is%20HTTP%3F/README.md)

| Метод | Назначение | В формах |
|-------|------------|----------|
| **GET** | Получить ресурс; параметры в URL | `method="get"` — поиск, фильтры |
| **POST** | Отправить данные в теле | `method="post"` — логин, файлы |
| **PUT** | Заменить ресурс | API, не HTML-формы |
| **PATCH** | Частичное обновление | API |
| **DELETE** | Удалить | API |
| **HEAD** | Только заголовки ответа | — |
| **OPTIONS** | Допустимые методы (CORS) | — |

```html
<form action="/search" method="get">
    <input name="q">
    <button type="submit">Искать</button>
</form>
```

Пароли и личные данные — только **POST** + **HTTPS**.
