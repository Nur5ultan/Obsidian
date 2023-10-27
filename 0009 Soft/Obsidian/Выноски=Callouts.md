---
tag: callouts, obsidian
---

### Выноски

Используйте выноски для включения дополнительного контента, не нарушая поток ваших заметок.

Чтобы создать выноску, добавьте `[!info]` в первую строку блочной цитаты, где `info` это _идентификатор типа_. Идентификатор типа определяет, как выглядит выноска. Чтобы просмотреть все доступные типы, обратитесь к [поддерживаемым типам](https://help.obsidian.md/Editing+and+formatting/Callouts#Supported%20types).

> [!info] 
> Here's a callout block. 
> It supports **Markdown**, [[Internal link|Wikilinks]], and [[Embed files|embeds]]! 
> ![[og-image.png]]

Выноски также изначально поддерживаются в [Obsidian Publish](https://help.obsidian.md/Obsidian+Publish/Introduction+to+Obsidian+Publish).

Примечание

> [!Note]
> Если вы также используете плагин Admonitions, вам следует обновить его по крайней мере до версии 8.0.0, чтобы избежать проблем с новой функцией выноски.


### Измените заголовок

По умолчанию заголовок выноски является идентификатором ее типа в регистре title. Вы можете изменить его, добавив текст после идентификатора типа:

> [!tip] Выноски могут иметь пользовательские названия
> Нравится эта.

Вы даже можете опустить текст, чтобы создать выноски только для заголовка:
> [!tip] Выноска только для заголовка

### Складные выноски

Выноску можно сделать складной, добавив плюс (+) или минус (-) непосредственно после идентификатора типа.

Знак "плюс" по умолчанию расширяет выноску, а знак "минус" вместо этого сворачивает ее.

> [!faq]- Являются ли выноски складными?? 
> Да! При сворачивании содержимое скрывается, когда оно сворачивается.

### Вложенные выноски

Выноски можно размещать на нескольких уровнях.

> [!question] Могут ли выноски быть вложенными?
> > [!todo] Да!, они могут.
> > > [!example]  Вы даже можете использовать несколько слоев вложенности.

### Настройка выноски
[Фрагменты CSS](https://help.obsidian.md/Extending+Obsidian/CSS+snippets) и [плагины сообщества](https://help.obsidian.md/Extending+Obsidian/Community+plugins) могут определять пользовательские выноски или даже перезаписывать конфигурацию по умолчанию.

Чтобы определить пользовательскую выноску, создайте следующий блок CSS:
```css
.callout[data-callout="custom-question-type"] { --callout-color: 0, 0, 0; --callout-icon: lucide-alert-circle; }
```

Значением `data-callout` атрибута является идентификатор типа, который вы хотите использовать, например `[!custom-question-type]`.

- `--callout-color` определяет цвет фона с помощью цифр (0-255) для красного, зеленого и синего цветов.
- `--callout-icon` может быть идентификатором значка из [lucide.dev](https://lucide.dev/) или элементом SVG.

> [!tip] Значки SVG
> Вместо значка Lucide вы также можете использовать элемент SVG в качестве значка выноски.
> 
> `--callout-icon: '<svg>...custom svg...</svg>';`


### Поддерживаемые типы
Вы можете использовать несколько типов выноски и псевдонимов. У каждого типа свой цвет фона и значок.

Чтобы использовать эти стили по умолчанию, замените `info` в примерах любой из этих типов, например `[!tip]` или `[!warning]`.

Если вы не [настроите выноски](https://help.obsidian.md/Editing+and+formatting/Callouts#Customize%20callouts), для любого неподдерживаемого типа по умолчанию используется `note` тип. Идентификатор типа не чувствителен к регистру.

> [!note] Примечание
> 
> `> [!note]`
> `> Lorem ipsum dolor sit amet`


> [!abstract] Аннотация
> `> [!abstract]`
> `> Lorem ipsum dolor sit amet`

Псевдонимы: `summary`, `tldr`

> [!info] Информация
> `> [!info]`
> `> Lorem ipsum dolor sit amet`

> [!todo]
> `> [!todo]`
> `> Lorem ipsum dolor sit amet`

> [!tip] Совет
> `> [!tip]` 
> `> Lorem ipsum dolor sit amet`

Псевдонимы: `hint`, `important`

> [!success] Успех
> `> [!success]`
> `> Lorem ipsum dolor sit amet`

Псевдонимы: `check`, `done`

> [!question] Вопрос
> `> [!question]`
> `> Lorem ipsum dolor sit amet`

Псевдонимы: `help`, `faq`

> [!warning] Предупрение
> `> [!warning]`
> `> Lorem ipsum dolor sit amet`

Псевдонимы: `caution`, `attention`

> [!failure] Сбой
> `> [!failure]`
> `> Lorem ipsum dolor sit amet`

Псевдонимы: `fail`, `missing`

> [!danger] Опасность
> `> [!danger]`
> `> Lorem ipsum dolor sit amet`

Псевдоним: `error`

> [!bug] Ошибка
> `> [!bug]`
> `> Lorem ipsum dolor sit amet`


> [!example] Пример
> `> [!example]`
> `> Lorem ipsum dolor sit amet`


> [!quote] Цитата
> `> [!quote]`
> `> Lorem ipsum dolor sit amet`

Псевдоним: `cite`





[[help obsidian]]
