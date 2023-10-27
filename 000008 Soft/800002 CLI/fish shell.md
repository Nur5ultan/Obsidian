Fish - это полностью оборудованная оболочка командной строки (например, bash или zsh), которая является интеллектуальной и удобной для пользователя. Fish поддерживает мощные функции, такие как подсветка синтаксиса, автоматическое внушение и завершение табуляции, которые просто работают, и ничего не нужно изучать или настраивать.

Если вы хотите сделать свою командную строку более продуктивной, более полезной и более увлекательной, не изучая кучу непонятного синтаксиса и параметров конфигурации, то fish может быть именно тем, что вы ищете!

## Настраиваем приветствие

При интерактивном запуске fish пытается запустить функцию [fish_greeting](https://fishshell.com/docs/current/cmds/fish_greeting.html). fish_greeting по умолчанию выводит простое приветствие. Вы можете изменить ее текст, изменив `$fish_greeting` переменную, например, используя [универсальную переменную](https://fishshell.com/docs/current/language.html#variables-universal):

`set -U fish_greeting`

или вы можете установить его [глобально](https://fishshell.com/docs/current/language.html#variables-scope) в [config.fish](https://fishshell.com/docs/current/language.html#configuration):

`set -g fish_greeting "Привет, незнакомец!"`

или вы можете написать сценарий, изменив функцию:

```shell
function fish_greeting
    random choice "Hello!" "Hi" "G'day" "Howdy"
end
```

сохраните это в конфигурации.fish или [файл функции](https://fishshell.com/docs/current/language.html#syntax-function-autoloading). Вы также можете использовать [funced](https://fishshell.com/docs/current/cmds/funced.html) и [funcsave](https://fishshell.com/docs/current/cmds/funcsave.html) для упрощения редактирования.

## Оболочка по умолчанию
Существует несколько способов переключиться на fish (или любую другую оболочку) по умолчанию.

Самый простой способ - настроить эмулятор вашего терминала (например, GNOME Terminal, Apple Terminal.app или Konsole) на прямой запуск fish. Ознакомьтесь с ее конфигурацией и установите программу для запуска в `/usr/local/bin/fish` (если там установлена fish - замените другое местоположение соответствующим образом).

В качестве альтернативы вы можете установить fish в качестве оболочки входа, чтобы она запускалась всеми входами в терминал, включая SSH.

Чтобы изменить свой логин shell на fish:
1. Добавьте панцирь в `/etc/shells` с:
	`echo /usr/local/bin/fish | sudo tee -a `
2. Измените оболочку по умолчанию с помощью:
	`chsh -s /usr/local/bin/fish`

Снова замените путь к fish на `/usr/local/bin/fish` - смотрите `command -s fish` внутри fish . Чтобы изменить его обратно на другую оболочку, просто замените `/usr/local/bin/fish` на `/bin/bash`, `/bin/tcsh` или `/bin/zsh` при необходимости в описанных выше шагах.


## Как мне запускать команду при каждом входе в систему? Что эквивалентно fish .bashrc или .profile?

Отредактируйте файл `~/.config/fish/config.fish` [[1]](https://fishshell.com/docs/current/faq.html#id2), создав его, если он не существует (обратите внимание на начальный период).

В отличие от .bashrc и .profile, этот файл всегда читается, даже в неинтерактивных оболочках или оболочках входа в систему.

Чтобы сделать что-то только в интерактивных оболочках, отметьте `status is-interactive`, как:

```shell
if status is-interactive
    # use the coolbeans theme
    fish_config theme choose coolbeans
end
```

