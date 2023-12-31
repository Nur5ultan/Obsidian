# Функциональность

Это расширение расширяет возможности редактирования кода HTML и ejs за счет `Go To Definition` и `Go To Symbol in Workspace` поддержки css / scss / less (классов и идентификаторов), содержащихся в строках исходного кода.

Это было во многом вдохновлено аналогичной функцией в [скобках](http://brackets.io/), называемой CSS Inline Editors.

![[Files/e0279f29d948c7effbbb2c777fcb4c6c_MD5.gif]]

Расширение поддерживает все обычные возможности отслеживания определений символов, но делает это для css-селекторов (классов, идентификаторов и HTML-тегов). Это включает в себя:

-   Просмотр: загрузите файл css встроенным и внесите быстрые изменения прямо там. (`Ctrl+Shift+F12`)
-   Перейдите по ссылке: перейдите непосредственно к файлу css или откройте его в новом редакторе (`F12`)
-   Наведение курсора мыши: отображение определения при наведении курсора мыши на символ (`Ctrl+hover`)

Кроме того, он поддерживает поставщика символов, поэтому вы можете быстро перейти к нужному коду CSS / SCSS / LESS, если вы уже знаете имя класса или идентификатора (для этого вам нужно ввести не менее 2 символов). Выполнение этой команды может занять несколько секунд, если у вас большие таблицы стилей)

![[Files/4c3130f4a8bea08c691f11c2cf9db690_MD5.gif]]

## Конфигурация

-   `cssPeek.supportTags` - Включить просмотр HTML-тегов в дополнение к именам классов и идентификаторам. Компоненты React игнорируются, но при использовании Angular рекомендуется отключить эту функцию.
-   `cssPeek.peekFromLanguages` - Список названий языков vscode, в которых следует использовать расширение.
-   `cssPeek.peekToExclude` - Список файловых глобусов, который отфильтровывает файлы стилей, чтобы их не искать. По умолчанию `node_modules` и `bower_components`

Более подробную информацию смотрите в документах редактора

-   [Код Visual Studio: определение Goto](https://code.visualstudio.com/docs/editor/editingevolved#_go-to-definition)
-   [Код Visual Studio: Peek](https://code.visualstudio.com/docs/editor/editingevolved#_peek)
-   [Код Visual Studio: Открыть символ по имени](https://code.visualstudio.com/Docs/editor/editingevolved#_open-symbol-by-name)