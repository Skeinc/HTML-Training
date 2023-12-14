# Цитаты и элементы цитирования в HTML

Веб-страницы часто включают цитаты, которые помогают подчеркнуть важность определенных высказываний или текстов. 

## HTML тег blockquote для цитат

Элемент ``<blockqoute>`` используется для выделения длинных цитат, которые распологаются в отдельном блоке. Этот элемент помогает создать визуальное отличие между цитатой и основным текстом страницы:

```
<p>Here is a quote from WWF's website:</p>
<blockquote cite="http://www.worldwildlife.org/who/index.html">
    For 60 years, WWF has worked to help people and nature thrive. As the world's leading conservation organization, WWF works in nearly 100 countries. At every level, we collaborate with people around the world to develop and deliver innovative solutions that protect communities, wildlife, and the places in which they live.
</blockquote>
```

## HTML тег q для коротких цитат

Элемент ``<q>`` предназначен для коротких цитат, которые выстраиваются непосредственно в текст. Браузеры автоматически добавляют кавычки вокруг текста, помеченного этим элементом:

```
<p>WWF's goal is to: <q>Build a future where people live in harmony with nature.</q></p>
```

## HTML тег abbr для аббревиатур

Элемент ``<abbr>`` определяет аббревиатуру или акроним, например "HTML", "CSS" и т.д. Маркировка сокращений может дать полезную информацию браузерам, перевод системы и поисковые системы. Используйте глобальный атрибут заголовка, чтобы показать описание к аббревиатуре при наведении курсора мыши на элемент:

```
<p>The <abbr title="World Health Organization">WHO</abbr> was founded in 1948.</p>
```

## HTML тег address для контактной информации

Элемент ``<address>`` определяет контактную информацию автора/владельца документа или статьи. Контактная информация может представлять собой адрес электронной почты, URL-адрес, физический адрес, телефон, номер, адрес социальной сети и т.д. Текст в элементе ``<address>`` обычно отображается курсивом и браузеры всегда добавляют разрыв строки до и после элемента ``<address>``:

```
<address>
    Written by John Doe.<br>
    Visit us at:<br>
    Example.com<br>
    Box 564, Disneyland<br>
    USA
</address>
```

## HTML тег cite для названия работ

Элемент ``<cite>`` используется для указания источника цитаты или названия произведения. Обычно он помещается внутрь элементов цитирования:

```
<p><cite>The Scream</cite> by Edvard Munch. Painted in 1893.</p>
```

## HTML тег bdo для двунаправленной блокировки

Элемент ``<bdo>`` используйте для переопределения текущего направления текста:

```
<bdo dir="rtl">This text will be written from right to left.</bdo>
```

## HTML атрибут cite

Элементы цитирования также могут содержать атрибут ``cite``, который указывает на источник цитаты. Это полезно для обеспечения доступности дополнительной информации:

```
<p>Here is a quote from WWF's website:</p>
<blockquote cite="http://www.worldwildlife.org/who/index.html">
    For 60 years, WWF has worked to help people and nature thrive. As the world's leading conservation organization, WWF works in nearly 100 countries. At every level, we collaborate with people around the world to develop and deliver innovative solutions that protect communities, wildlife, and the places in which they live.
</blockquote>
```

## Заключение

Цитаты играют важную роль в веб-разработке, помогая выделить важные и многозначительные высказывания. С использованием элементов цитирования и атрибута ``cite`` вы можете структурировать цитаты на своих веб-страницах, делая контент более читаемым и информативным.