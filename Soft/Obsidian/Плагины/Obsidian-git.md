## [Obsidian Git](https://github.com/denolehov/obsidian-git#obsidian-git)

Плагин, позволяющий создавать резервные копии вашего [Obsidian.md](https://obsidian.md/) хранилища в удаленном репозитории Git (например, частном репозитории на GitHub).

Требования, шаги по установке (включая настройку для мобильных устройств), советы и рекомендации, распространенные проблемы и многое другое можно найти в [документации](https://publish.obsidian.md/git-doc).

Для мобильных пользователей смотрите раздел "[Мобильные](https://github.com/denolehov/obsidian-git#mobile) устройства" ниже.

## [Выделенные функции](https://github.com/denolehov/obsidian-git#highlighted-features)

-   Автоматическое резервное копирование хранилища каждые X минут
-   Извлеките изменения из удаленного репозитория при запуске Obsidian
-   Назначьте горячие клавиши для переноса изменений в удаленный репозиторий
-   Управляйте различными репозиториями с помощью подмодулей Git (после включения этой функции в настройках)
-   Режим управления версиями позволяет создавать и фиксировать отдельные файлы. Его можно открыть с помощью `Open Source Control View` команды.
-   В представлении истории отображаются коммиты и измененные ими файлы. То есть, по сути, интегрированное хранилище `git log`. Его можно открыть с помощью `Open History View` команды.
-   Для просмотра истории файла я настоятельно рекомендую вам плагин Version History Diff

### [Представление системы управления версиями](https://github.com/denolehov/obsidian-git#source-control-view)

[![Представление системы управления версиями](https://raw.githubusercontent.com/denolehov/obsidian-git/master/images/source-view.png)](https://raw.githubusercontent.com/denolehov/obsidian-git/master/images/source-view.png)

### [Просмотр истории](https://github.com/denolehov/obsidian-git#history-view)

[![Просмотр истории](https://raw.githubusercontent.com/denolehov/obsidian-git/master/images/history-view.png)](https://raw.githubusercontent.com/denolehov/obsidian-git/master/images/history-view.png)

## [Доступные команды](https://github.com/denolehov/obsidian-git#available-commands)

-   Изменения
    -   `List changed files`: Перечисляет все изменения в модальном
    -   `Open diff view`: Откройте diff view для текущего файла
    -   `Stage current file`
    -   `Unstage current file`
-   Фиксация
    -   `Commit all changes`: Только фиксирует все изменения без нажатия
    -   `Commit all changes with specific message`: То же, что и выше, но с пользовательским сообщением
    -   `Commit staged`: фиксирует только файлы, которые были созданы заранее
    -   `Commit staged with specific message`: То же, что и выше, но с пользовательским сообщением
-   Резервное копирование
    -   `Create Backup`: Фиксирует все изменения. Если включена настройка "Принудительное резервное копирование", также будет принудительное выполнение фиксации.
    -   `Create Backup with specific message`: То же, что и выше, но с пользовательским сообщением
    -   `Create backup and close`: То же, что `Create Backup`, но при запуске на рабочем столе окно Obsidian закроется. Приложение Obsidian на мобильном устройстве не выйдет.
-   Удаленно
    -   `Push`
    -   `Pull`
    -   `Edit remotes`
    -   `Remove remote`
    -   `Clone an existing remote repo`: Открывает диалоговое окно, в котором запрашивается URL-адрес и аутентификация для клонирования удаленного репозитория
    -   `Open file on GitHub`: Откройте файловое представление текущего файла на GitHub в окне браузера. Примечание: работает только на рабочем столе
    -   `Open file history on GitHub`: Откройте историю файлов текущего файла на GitHub в окне браузера. Примечание: работает только на рабочем столе
-   Местные новости
    -   `Initialize a new repo`
    -   `Create new branch`
    -   `Delete branch`
    -   `CAUTION: Delete repository`
-   Представление системы управления версиями
    -   `Open source control view`: Открывает боковую панель, отображающую [представление системы управления версиями](https://github.com/denolehov/obsidian-git#sidebar-view)
    -   `Edit .gitignore`
    -   `Add file to .gitignore`: Добавьте текущий файл в .gitignore

## [Для рабочего стола](https://github.com/denolehov/obsidian-git#desktop)

## [Аутентификация](https://github.com/denolehov/obsidian-git#authentication)

Аутентификация может потребовать дополнительной настройки. Подробнее смотрите в [документации по аутентификации](https://publish.obsidian.md/git-doc/Authentication)

### [Obsidian в Linux](https://github.com/denolehov/obsidian-git#obsidian-on-linux)

-   ⚠ Snap не поддерживается.
-   Не рекомендуется использовать Flatpak, поскольку он не имеет доступа ко всем системным файлам.

Пожалуйста, используйте вместо этого AppImage ([руководство по установке Linux](https://publish.obsidian.md/git-doc/Installation#Linux))

## [Мобильный](https://github.com/denolehov/obsidian-git#mobile)

### [Ограничения мобильной версии](https://github.com/denolehov/obsidian-git#restrictions-of-the-mobile-version)

Я использую [isomorphic-git](https://isomorphic-git.org/), который является повторной реализацией Git в JavaScript, потому что вы не можете использовать native Git на Android или iOS.

-   Аутентификация по SSH не поддерживается ([проблема с isomorphic-git](https://github.com/isomorphic-git/isomorphic-git/issues/231))
-   Размер репозитория ограничен из-за ограничений памяти
-   Стратегия повторного объединения не поддерживается
-   Подмодули не поддерживаются

### [Производительность на мобильных устройствах](https://github.com/denolehov/obsidian-git#performance-on-mobile)

Предупреждение  
В зависимости от вашего устройства и доступной свободной оперативной памяти Obsidian может аварийно завершать работу при клонировании / извлечении. Я не знаю, как это исправить. Если это так для вас, я должен признать, что этот плагин не будет работать для вас. Поэтому комментирование любой проблемы или создание новой не поможет. Прошу прощения.

**Настройка:** iPad Pro M1 с [хранилищем](https://github.com/Vinzent03/obsidian-git-stress-test) из 3000 файлов, уменьшенных с [10000 файлов markdown](https://github.com/Zettelkasten-Method/10000-markdown-files)

Начальное копирование заняло 0 минут 25 секунд. После этого наиболее трудоемкой частью является проверка всего рабочего каталога на предмет изменений файлов. При этой настройке проверка всех файлов на предмет изменений в stage занимает 03 минуты 40 секунд. Другие команды, такие как pull, push и commit, выполняются очень быстро (1-5 секунд).

Самый быстрый способ работы на мобильных устройствах, если у вас большое хранилище, - создавать отдельные файлы и фиксировать только промежуточные файлы.

## [Контакты](https://github.com/denolehov/obsidian-git#contact)

Функция создания строк была разработана [GollyTicker](https://github.com/GollyTicker), поэтому на любые вопросы лучше всего ответить у него.

Если у вас есть какие-либо отзывы или вопросы, не стесняйтесь обращаться через GitHub issues или `@Vinadon` на [сервере Obsidian Discord](https://discord.com/invite/veuWUTm).

Изначально этот плагин был разработан [denolehov](https://github.com/denolehov). С марта 2021 года разработкой этого плагина занимается [Vinzent03](https://github.com/Vinzent03).

Если вы хотите поддержать меня ([Vinzent03](https://github.com/Vinzent03)), вы можете поддержать меня на Ko-fi

[![ko-fi](https://camo.githubusercontent.com/cd07f1a5d90e454e7bbf69d22ebe4cdbd3a0b3dcf56ba0b6c2495a8e99c776be/68747470733a2f2f6b6f2d66692e636f6d2f696d672f676974687562627574746f6e5f736d2e737667)](https://ko-fi.com/F1F195IQ5)