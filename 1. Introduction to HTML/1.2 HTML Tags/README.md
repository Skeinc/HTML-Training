# HTML теги

Теги HTML подобны ключевым словам, которые определяют, как веб-браузер будет форматировать и отображать контент. С помощью тегов веб-браузер может различать HTML-контент и простой контент. HTML-теги состоят из трех основных частей: открывающего тега, содержимого и закрывающего тега. Но некоторые HTML-теги являются незакрытыми.

HTML-теги являются важными элементами для создания веб-страниц. Это специальные ключевые слова, которые используются для создания визуальных элементов на веб-странице. Они формируют синтаксис языка HTML и используются для создания визуальных элементов, таких как текст, ввод, кнопки и т.д., на веб-странице.

Каждый тег HTML имеет уникальное назначение, свойства и вариант использования. Например, тег ``<img>`` используется для отображения изображения на странице. Но тег ``<p>`` используется для отображения абзаца на веб-странице.

## Компоненты HTML-тегов

Каждый HTML-тег состоит из следующих компонентов:
1. **Набор открывающей (``<>``) и закрывающей угловой скобки ``</>``**
2. **Название тега** 
3. **Содержимое тега**

## Синтаксис HTML-тегов

Каждый тег HTML начинается с пары открывающих угловых скобок (``<>``). Между этими скобками следует имя тега.

Конец тега обозначается парой закрывающих угловых скобок (``</>``), между которыми находится имя тега.

Внутри этих скобок следуйте содержимому тега:

```
<tagname>
    <!-- Tag's content -->
</tagname>
```

## Содержимое внутри HTML-тега

Содержимое между закрывающим и открывающим HTML-тегами определяет поведение этого конкретного тега.

Например, тег ``<h1>`` обозначает большой заголовок. Содержимое внутри этого тега будет иметь свойство тега ``<h1>``.

```
<h1>
    This is a large heading
</h1>
```

Таким образом, приведенный выше HTML-код выведет на веб-страницу большой заголовок.

## Примечания

1. **Никогда не пропускайте конечный тег:** Некоторые элементы HTML будут отображаться правильно, даже если вы забудете закрывающий тег. Однако никогда не полагайтесь на это! Если вы забудете конечный тег, могут возникнуть неожиданные результаты и ошибки!
2. **Пустые HTML-элементы:** HTML-элементы без содержимого называются пустыми элементами. Тег ``<br>`` определяет разрыв строки и представляет собой пустой элемент без закрывающего тега:

```
<p>This is a<br> paragraph with a line breal.</p>
```

3. **HTML не чувствителен к регистру:** HTML-теги не чувствительны к регистру: ``<P>`` означает то же самое, что и ``<p>``. Стандарт HTML не требует использования тегов в нижнем регистре, но рекомендуется использовать строчные буквы в HTML и требуется использовать строчные буквы для более строгих типов документов, например, XHTML.