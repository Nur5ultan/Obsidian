Obsidian - отличное приложение для ведения заметок. Встроенные функции превосходны и их более чем достаточно для базовых целей ведения заметок. _Однако_, если вы хотите получить от Obsidian _больше_ — если вы хотите [наделить Obsidian сверхспособностями](https://obsidian.rocks/super-powers-for-obsidian-nine-of-the-best-obsidian-plugins/) как таковыми, — тогда вам _нужно_ ознакомиться с Dataview.

Из всех замечательных плагинов сообщества Dataview - мой любимый. Dataview позволяет мне _автоматизировать_ некоторые аспекты моего хранилища, особенно то, что было бы утомительно или сложно выполнять вручную.

Например, Dataview позволяет мне [быстро и без усилий создавать MOC-файлы](https://obsidian.rocks/quick-tip-quickly-organize-notes-in-obsidian/). Один только этот прием значительно упростил мне организацию моих заметок.

Вот несколько других примеров того, что я делаю с Dataview:

-   Перечислите задачи, которые должны быть выполнены сегодня
-   Перечислите предстоящие дни рождения людей в моем хранилище
if(typeof ez\_ad\_units == 'undefined'){ez\_ad\_units=\[\];}ez\_ad\_units.push(\[\[300,250\],'obsidian\_rocks-medrectangle-4','ezslot\_0',111,'0','0', 'obsidian\_rocks-medrectangle-4-0'\]);if(typeof \_\_ez\_fad\_position == 'function'){\_\_ez\_fad\_position('div-gpt-ad-obsidian\_rocks-medrectangle-4-0');}![[Files/634511236e6ab68303bec80892e372e7_MD5.png|"ezoic"]]-   Создайте таблицу, в которой будут показаны ежедневные или еженедельные достижения целей
-   Создавайте [динамические графики, показывающие показатели из моего хранилища](https://obsidian.rocks/creating-dynamic-graphs-in-obsidian/)
-   И многое другое
if(typeof ez\_ad\_units == 'undefined'){ez\_ad\_units=\[\];}ez\_ad\_units.push(\[\[250,250\],'obsidian\_rocks-box-4','ezslot\_1',112,'0','0', 'obsidian\_rocks-box-4-0'\]);if(typeof \_\_ez\_fad\_position == 'function'){\_\_ez\_fad\_position('div-gpt-ad-obsidian\_rocks-box-4-0');}![[Files/634511236e6ab68303bec80892e372e7_MD5.png|"ezoic"]]

Хотите узнать, как автоматизировать свое собственное хранилище с помощью Dataview? Что ж, тогда давайте начнем.

Writesonic: Boosting Your Business ...

Please enable JavaScript

[Writesonic: Boosting Your Business Like Never Before!](https://humix.com/redirect?url=https%3A%2F%2Ffirefortuna.com%2Fhumix%2Fvideo%2FesNF5skJ5O2)

## Содержание

-   [Основы просмотра данных](https://obsidian.rocks/dataview-in-obsidian-a-beginners-guide//#fundamentals)
-   [Ограничение ваших запросов](https://obsidian.rocks/dataview-in-obsidian-a-beginners-guide//#limiting-queries)
if(typeof ez\_ad\_units == 'undefined'){ez\_ad\_units=\[\];}ez\_ad\_units.push(\[\[250,250\],'obsidian\_rocks-banner-1','ezslot\_3',113,'0','0', 'obsidian\_rocks-banner-1-0'\]);if(typeof \_\_ez\_fad\_position == 'function'){\_\_ez\_fad\_position('div-gpt-ad-obsidian\_rocks-banner-1-0');}![[Files/634511236e6ab68303bec80892e372e7_MD5.png|"ezoic")-   [Типы данных в Dataview](https://obsidian.rocks/dataview-in-obsidian-a-beginners-guide//#types-of-data]]
    -   [Встроенные данные](https://obsidian.rocks/dataview-in-obsidian-a-beginners-guide//#built-in-data)
    -   [Добавление пользовательских данных в ваши заметки](https://obsidian.rocks/dataview-in-obsidian-a-beginners-guide//#custom-data)
-   [Исключение результатов из вашего запроса](https://obsidian.rocks/dataview-in-obsidian-a-beginners-guide//#removing-results)
    -   [Фильтрация](https://obsidian.rocks/dataview-in-obsidian-a-beginners-guide//#filtering)
    -   [Сортировка](https://obsidian.rocks/dataview-in-obsidian-a-beginners-guide//#sorting)
    -   [Ограничение](https://obsidian.rocks/dataview-in-obsidian-a-beginners-guide//#limiting)
    if(typeof ez\_ad\_units == 'undefined'){ez\_ad\_units=\[\];}ez\_ad\_units.push(\[\[250,250\],'obsidian\_rocks-leader-1','ezslot\_2',115,'0','0', 'obsidian\_rocks-leader-1-0'\]);if(typeof \_\_ez\_fad\_position == 'function'){\_\_ez\_fad\_position('div-gpt-ad-obsidian\_rocks-leader-1-0');}![[Files/634511236e6ab68303bec80892e372e7_MD5.png|"ezoic"]]
-   [Задачи и просмотр данных](https://obsidian.rocks/dataview-in-obsidian-a-beginners-guide//#tasks-and-dataview)
-   [Не интересуетесь основами и болтами? Начните здесь.](https://obsidian.rocks/dataview-in-obsidian-a-beginners-guide//#examples)
-   [Заключение / Дополнительные ресурсы](https://obsidian.rocks/dataview-in-obsidian-a-beginners-guide//#resources)

## Основы просмотра данных

Начать работу с Dataview может быть непросто. Но если у вас настроено хранилище Obsidian vault с несколькими файлами в нем, то у вас есть все необходимое для начала. Если нет, попробуйте загрузить [это практическое хранилище](https://github.com/s-blu/obsidian_dataview_example_vault).

Для начала важно помнить, что Dataview помогает вам _просматривать_ данные, но не _редактировать_ их. _Запрос Dataview_ извлекает заметки из вашего хранилища, но никогда не _изменяет_ их, поэтому нет риска уничтожить ваши с трудом заработанные заметки с помощью Dataview.

> Примечание: появилась новая версия Dataview под названием [Datacore](https://github.com/blacksmithgu/datacore), созданная тем же разработчиком. Datacore обещает помочь вам редактировать данные лучше, чем Dataview. Он еще не готов к выходу в прайм-тайм, но мы напишем об этом, когда это будет сделано.

Существует четыре основных _формата_, которые вы можете использовать для отображения данных в Dataview. Это:

-   Таблица
-   Список
-   Задание
-   Календарь

Теперь, если мы запустим запрос с каждым из этих форматов, результаты будут выглядеть по-разному. У нас есть те же данные, но Dataview отображает их в запрошенном формате. Четыре различных формата, предлагаемых Dataview, выглядят примерно так:

![[Files/bbd9fc82984e2d46ee57208df8c7ec8a_MD5.jpg]]

![An image that shows the four different formats offered by Dataview: Calendar, List, Table, and Tasks.](data:image/svg+xml,%3Csvg%20xmlns='http://www.w3.org/2000/svg'%20viewBox='0%200%201024%20512'%3E%3C/svg%3E)

Четыре формата, предлагаемые Dataview.

Обычно вы используете запросы к таблице или списку. Два других являются более ситуационными.

Кроме того, format является _единственной обязательной командой_ в Dataview. Ваш первый запрос Dataview может быть таким простым, как этот:

````
```dataview
LIST 
\```
````

Приведенный выше запрос создаст список, включающий _все файлы в вашем хранилище_.

_Но_ если у вас большое хранилище, этот запрос выполняется медленно и не очень полезно. Обычно вам нужно _ограничить_ свой запрос определенной папкой. Давайте поговорим об этом дальше.

## Ограничение ваших запросов к просмотру данных

Обычно вы не хотите просматривать _все_ заметки в вашем хранилище с помощью заданного запроса Dataview. Вы захотите _ограничить область_ вашего запроса, используя _источник_.

### Ограничение по папкам

Включение источника указывает Dataview, где искать данные, которые вы пытаетесь извлечь. Самый простой источник - это папка, и вы можете ограничить поиск папкой, используя этот синтаксис:

````
```dataview
LIST
FROM "A Folder"
\```
````

Обратите внимание на кавычки: кавычки указывают Dataview на поиск файла или папки. Вы также можете ограничить его отдельными файлами или вложенными папками, используя стандартный синтаксис файла. Например. `FROM "A Folder/Subfolder"` или `FROM "A Folder/Subfolder/File.md"`

### Ограничение по тегам

Еще один способ ограничить ваши результаты - использовать теги. В Obsidian вы можете добавить тег к любому файлу, используя хэштег, например `#tag`. Затем вы можете извлекать любые файлы, содержащие этот тег, с помощью Dataview:

````
```dataview
LIST
FROM #tag
\```
````

> Примечание: вы также можете выполнять поиск по тегам с помощью встроенного плагина поиска. Если вы не совсем готовы использовать Dataview, [взгляните на встроенные поисковые запросы](https://obsidian.rocks/obsidian-search-five-hidden-features/#embedded-search).

Поиск по тегам также полезен с помощью _вложенных тегов_. Я считаю очень полезным использовать [вложенные теги для статусов проектов](https://obsidian.rocks/how-to-manage-projects-in-obsidian/), и тогда я могу извлекать _все проекты_, используя `#project` тег, или я могу привязать его к определенному статусу, такому как `#project/soon` или `#project/active`. Вложенные теги отлично подходят для указания статуса файла, независимо от того, занимаетесь ли вы \[\[выращиванием своего цифрового сада\]\] или управляете проектами.

### Комбинирование источников

Папки и теги - это два основных способа _получения_ данных с помощью Dataview. Но вы также можете _комбинировать_ эти два источника для выполнения более сложных запросов. Вы можете сделать это с помощью операторов `AND` и `OR`. Вы также можете использовать круглые скобки для указания логического порядка этих утверждений (это как математика в старших классах: все, что указано в круглых скобках, идет первым):

````
```dataview
LIST
FROM "Projects" AND (#project/active OR #project/soon) 
\```
````

## Различные типы данных в Dataview

Далее нам нужно поговорить о различных типах данных в Dataview.

Есть одна вещь, которую вы не можете запросить в Dataview: _содержимое_ ваших заметок. Чтобы ускорить просмотр данных, вы не сможете выполнять поиск по фактическому _содержимому_ ваших заметок с помощью Dataview. Это звучит как серьезное ограничение, но при некотором тщательном обдумывании и внимании это не так сложно, как кажется. Если вы _действительно_ хотите встроить результаты поиска в свои заметки, вы можете сделать это с [помощью встроенного плагина поиска](https://obsidian.rocks/obsidian-search-five-hidden-features/).

Что _делает_ Dataview, так это включает в себя множество _встроенных метаданных_ для каждой из ваших заметок, позволяя вам быстро извлекать свои заметки на основе любого количества различных факторов. Кроме того, вы можете добавлять в заметки свои _собственные_ метаданные, если вам это необходимо. Давайте рассмотрим эти два типа данных.

### Встроенные данные

Dataview предоставляет вам массу возможностей для управления с помощью множества _встроенных_ метаданных для всех ваших заметок. Как только вы включаете плагин Dataview, он автоматически создает эти данные, так что вы можете использовать его в любое время. Вот полный список всех данных, которые создает Dataview, позаимствованный [из документации](https://blacksmithgu.github.io/obsidian-dataview/annotation/metadata-pages/):

| Название поля | Описание |
| --- | --- |
| `file.name` | Имя файла указано на боковой панели Obsidians. |
| `file.folder` | Путь к папке, к которой относится этот файл. |
| `file.path` | Полный путь к файлу, включая имя файла. |
| `file.ext` | Расширение типа файла; обычно `md`. |
| `file.link` | Ссылка на файл. |
| `file.size` | Размер файла (в байтах). |
| `file.ctime` со временем | Дата создания файла. |
| `file.cday` | Дата создания файла. |
| `file.mtime` со временем | Дата последнего изменения файла. |
| `file.mday` | Дата последнего изменения файла. |
| `file.tags` | Список всех уникальных тегов в заметке. Вложенные теги разбиты по каждому уровню, поэтому `#Tag/1/A` будут сохранены в списке как `[#Tag, #Tag/1, #Tag/1/A]`. |
| `file.etags` | Список всех явных тегов в заметке; в отличие от `file.tags`, не разбивает подтеги, т.е. `[#Tag/1/A]` |
| `file.inlinks` | Список всех входящих ссылок на этот файл, то есть всех файлов, содержащих ссылку на этот файл. |
| `file.outlinks` | Список всех исходящих ссылок из этого файла, то есть всех ссылок, содержащихся в файле. |
| `file.aliases` | Список всех псевдонимов для заметки, определенных с помощью [YAML frontmatter](https://help.obsidian.md/How+to/Add+aliases+to+note). |
| `file.tasks` | Список всех заданий (т.е. `|[ ] some task`) в этом файле. |
| `file.lists` | Список всех элементов списка в файле (включая задачи); эти элементы фактически являются задачами и могут быть отображены в представлениях задач. |
| `file.frontmatter` | Содержит исходные значения всех frontmatter в виде `key |value` текстовых значений; в основном полезен для проверки исходных значений frontmatter или для динамического перечисления ключей frontmatter. |
| `file.day` | Доступно только в том случае, если в имени файла указана дата (формы `yyyy-mm-dd` или `yyyymmdd`) или есть `Date` поле / встроенное поле. |
| `file.starred` | если этот файл был выделен с помощью плагина Obsidian Core “Выделенные файлы”. |

Неплохо сохранить приведенную выше таблицу в качестве примечания для собственного ознакомления. При работе с Dataview ее удобно иметь под рукой. ([вот уцененная версия, которую вы можете скопировать / вставить](https://gist.githubusercontent.com/WebInspectInc/589bbd8aca2b1a4cdb1d03c8187d33de/raw/b3946f26ea3c49016c5b9c32ce0dae8abbfc7782/dataview-implicit-types.markdown))

Любые из приведенных выше данных могут быть использованы в любом запросе Dataview. Например, мы могли бы создать таблицу со всеми нашими отмеченными звездочками примечаниями, подобную этой:

````
```dataview
TABLE file.starred AS "⭐"
WHERE file.starred = true
\```
````

> Примечание: Обратите внимание, что заголовки таблиц можно изменять с помощью ключевого слова AS. В приведенном выше примере именем таблицы будет значок в виде звездочки, а не "file.starred” по умолчанию.

### Добавление пользовательских данных в ваши заметки

В дополнение к приведенным выше данным вы также можете добавить свои собственные данные в любую заметку. Вы можете использовать это для всего, что только можете себе представить. Чтобы добавить пользовательские данные, вы можете либо добавить свойства, либо использовать синтаксис двойного двоеточия.

Свойства добавляются в верхней части вашего документа (или на боковой панели) и полезны для самых разных целей. Если вы не знакомы со свойствами, ознакомьтесь с нашим [введением в свойства обсидиана](https://obsidian.rocks/an-introduction-to-obsidian-properties/) и [пятью профессиональными советами по свойствам обсидиана](https://obsidian.rocks/five-pro-tips-for-obsidian-properties/).

Свойства становятся чище, если вам нужно добавить _много_ данных, но если у вас есть только несколько элементов, то Dataview имеет другой синтаксис, который _используется только_ для Dataview. Эти данные можно добавить _в любое_ место в вашей заметке, и они выглядят примерно так:

```
date:: 202302280654
aliases:: ['data']
status:: Idea
```

С помощью Dataview можно запросить как свойства, так и метаданные, приведенные выше, следующим образом:

````
```dataview
LIST
WHERE status = "Idea"
\```
````

## _Удаление_ результатов из вашего запроса

В двух приведенных выше запросах используется оператор WHERE, о котором мы еще не говорили. WHERE - это один из способов _исключить_ результаты из запроса.

Исключение результатов - вот где происходит волшебство. Просмотр заметок по тегам или папкам - это прекрасно, с этим мало что можно сделать. Отфильтровывать результаты на основе данных — _это_ хорошо.

### Как фильтровать результаты

Фильтрация - это самый сложный, но и самый гибкий способ исключения объектов из вашего поиска. Фильтрация позволяет исключать заметки на основе данных внутри самой заметки. Возвращаясь к приведенным выше примерам, вы можете создавать списки или таблицы, используя любые встроенные данные, например, просматривать все ваши отмеченные звездочками заметки:

````
```dataview
LIST
WHERE file.starred = true
\```
````

Вы также можете извлекать заметки на основе времени их последнего изменения. Один запрос, который я нахожу полезным, показывает список всех заметок, которые я отредактировал за последнюю неделю:

````
```dataview
LIST
WHERE file.mtime >= date(today) - dur(1 week)
\```
````

Это немного сложнее, но может быть чрезвычайно полезным. Приведенный выше запрос проверяет “mtime” (время последнего _изменения_ файла) и сравнивает его со вчерашней датой. Если файл не был изменен за последний день, это исключит его из результатов.

Предложение WHERE позволяет проверять _любые_ данные в _любой_ заметке. Сюда входят _встроенные_ данные, а также пользовательские данные. Если вам нужно исключить файлы на основе данных внутри самой заметки, ГДЕ можно это сделать?

> Примечание: Часто бывает, что вы используете ТО, ОТКУДА вам не нужно использовать, но ограничение вашего запроса определенной папкой или тегом _может_ ускорить ваш запрос, если кажется, что он выполняется медленно.

### Результаты сортировки

Иногда вы можете захотеть, чтобы ваши результаты отображались в порядке, отличном от установленного по умолчанию. Если это так, то вам понадобится ключевое слово SORT. Вы можете выполнить сортировку по любому полю и выбрать либо DESC, либо ASC.

````
```dataview
LIST
FROM #tag
SORT file.name ASC
\```
````

### Ограничение

Вы также можете _ограничить_ любой запрос, если он возвращает слишком много результатов. Это особенно удобно для больших запросов и может помочь ускорить работу с медленным документом. Синтаксис прост, вы можете использовать здесь любое целое число:

````
```dataview
LIST
FROM #tag
LIMIT 10
\```
````

## Задачи и просмотр данных

Проницательные читатели могут заметить, что мы еще не обсуждали задачи. Я хотел бы затронуть это здесь.

Когда я впервые начал использовать Dataview, я активно использовал запрос TASK. Но в наши дни у меня есть другое и, как мне кажется, лучшее решение.

Я уже писал обо всем моем [решении для управления задачами](https://obsidian.rocks/how-to-manage-tasks-in-obsidian/) ранее, и оно включает просмотр данных. Но большинство самих задач управляются с помощью [плагина Tasks](https://github.com/obsidian-tasks-group/obsidian-tasks), который, как я нахожу, работает намного лучше, чем Dataview. У задач также есть динамические запросы, подобные Dataview, но они гораздо более интерактивны и полезны, чем запросы Dataview. [Узнайте больше об управлении задачами здесь](https://obsidian.rocks/creating-a-today-view-in-obsidian/).

## Не интересуетесь основами и болтами? Вот несколько "рецептов”, которые помогут вам начать

Возможно, на этом этапе вы будете ошеломлены, и это нормально. Dataview - сложный плагин с бесконечным количеством применений, и может потребоваться много времени, чтобы освоиться с ним.

Вот несколько готовых запросов, которые вы можете скопировать / вставить в свое хранилище и которые могут оказаться полезными для вас. Убедитесь, что у вас [установлен и включен](https://obsidian.rocks/how-to-use-community-plugins-in-obsidian/) Dataview, прежде чем пробовать что-либо из этого.

### Список файлов, созданных за последнюю неделю

````
```dataview
TABLE file.ctime AS "Created"
WHERE file.ctime >= date(today) - dur(1 week)
\```
````

### Список помеченных заметок в порядке последних правок

Замените `#tag` своим собственным тегом, и это покажет вам все примечания с `#tag` в порядке последних правок:

````
```dataview
LIST FROM #tag
SORT file.mtime DESC
\```
````

### Список несвязанных файлов

Это один из моих [любимых способов создания MOC](https://obsidian.rocks/quick-tip-quickly-organize-notes-in-obsidian/):

````
```dataview
list from [[]] and !outgoing([[]])
\```
````

Это создаст список всех файлов, которые ссылаются на текущий файл, но у которых _еще нет_ ссылки в файле. Это отличный способ [избежать потери файлов в вашем Zettelkasten](https://obsidian.rocks/getting-started-with-zettelkasten-in-obsidian/).

### Составьте список записей тренировок (или любой другой привычки!)

Для этого требуется использовать плагин Daily Notes. Если вы используете плагин Daily Notes, вы можете добавлять тренировки (или любую ежедневную привычку) в свои ежедневные заметки и отображать свой прогресс в таблице, подобной этой:

````
```dataview
TABLE workout
FROM "2 Areas/Journal/Daily Notes"
SORT file.ctime DESC
LIMIT 14
\```
````

### Список выполненных заданий

Несмотря на то, что большая часть управления моими задачами выполняется с помощью плагина Tasks, есть несколько уникальных функций, основанных на задачах, которые Dataview привносит в таблицу. Например, вы можете перечислить десять самых старых и незавершенных задач в вашем хранилище следующим образом:

````
```dataview
TASK
WHERE !completed
LIMIT 10
GROUP BY file.link
SORT rows.file.ctime ASC
\```
````

### Редактирование встроенных таблиц просмотра данных

Dataview - это в первую очередь инструмент для _просмотра_ данных, а не для их _редактирования_. Но с помощью пары хитрых приемов вы можете использовать его и для того, и для другого.

Если вы используете много таблиц в Dataview и хотите иметь возможность быстро редактировать содержимое внутри этих таблиц, вы можете ознакомиться с [тем, как редактировать таблицы Dataview встроенно](https://obsidian.rocks/editing-dataview-tables-with-the-metadata-menu-plugin/). Это продвинутый трюк, но для определенных людей его настройка определенно того стоит.

## Заключение и дополнительные ресурсы

Dataview - это невероятный и мощный плагин, который предоставляет вам множество различных инструментов для лучшего понимания и просмотра ваших заметок. Если вы еще не пробовали его раньше, я надеюсь, что эта статья придаст вам уверенности в том, что вы сможете это сделать.

Если вы застряли или у вас возникли проблемы, не стесняйтесь задавать вопросы в комментариях ниже или [на форуме](https://forum.obsidian.md/). Кроме того, вот несколько ресурсов, которые могут быть полезны, если вы хотите узнать больше:

-   [Документация по просмотру данных](https://blacksmithgu.github.io/obsidian-dataview/)
-   [Хранилище примеров просмотра данных](https://s-blu.github.io/obsidian_dataview_example_vault/) (здесь много хороших идей и вдохновения)
-   [Базовый конструктор запросов Dataview](https://s-blu.github.io/basic-dataview-query-builder/)