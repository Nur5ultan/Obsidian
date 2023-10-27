# Импортируйте расширение сортировки для кода Visual Studio с помощью `isort`

Расширение кода Visual Studio, обеспечивающее сортировку импорта с помощью `isort`. Расширение поставляется вместе с `isort=5.11.5`. Это расширение использует Language Server Protocol ([LSP](https://microsoft.github.io/language-server-protocol/)) для работы `isort` в серверном режиме.

Примечание:

-   Это расширение поддерживается для всех [активно поддерживаемых версий](https://devguide.python.org/#status-of-python-branches) `python` языка (т.е. python >= 3.7).
-   Входящий в комплект `isort` используется только в том случае, `isort` если в выбранной `python` среде нет установленной версии.
-   Минимальная поддерживаемая версия `isort` is `5.10.1`.

## Использование

После установки в Visual Studio Code расширение зарегистрируется `isort` как import organizer. Вы можете использовать сокращение с клавиатуры `shift` + `alt` + `O`, чтобы запустить действие редактора organize imports. Вы также можете запустить это из быстрого исправления, доступного, когда импорт не организован.

![Исправлена сортировка импорта с помощью действия кода.](https://github.com/microsoft/vscode-isort/raw/HEAD/images/vscode-isort.gif)

### Импортируйте сортировку при сохранении

Вы можете включить сортировку импорта при сохранении для python, указав в настройках следующие значения. Это добавит как сортировку импорта, так и форматирование (с помощью `black`) при сохранении :

```json
  "[python]": {
    "editor.defaultFormatter": "ms-python.black-formatter",
    "editor.formatOnSave": true,
    "editor.codeActionsOnSave": {
        "source.organizeImports": true
    },
  },
  "isort.args":["--profile", "black"],
```

### Отключение `isort` расширения

Если вы хотите отключить расширение isort, вы можете [отключить это расширение](https://code.visualstudio.com/docs/editor/extension-marketplace#_disable-an-extension) для каждой рабочей области в Visual Studio Code.

## Настройки
|Settings|Default|Description|
|---|---|---|
|isort.args|`[]`|Custom arguments passed to `isort`. E.g `"isort.args" = ["--settings-file", "<file>"]`|
|isort.check|`false`|Runs `isort --check` on open files and reports sorting issues as `Hint`. Update `isort.severity` to show sorting issues with higher severity.|
|isort.severity|`{ "W": "Warning", "E": "Hint" }`|Controls mapping of severity from `isort` to VS Code severity when displaying in the problems window.|
|isort.path|`[]`|Setting to provide custom `isort` executable. This will slow down formatting, since we will have to run `isort` executable every time or file save or open. Example 1: `["~/global_env/isort"]` Example 2: `["conda", "run", "-n", "lint_env", "python", "-m", "isort"]`|
|isort.interpreter|`[]`|Path to a python interpreter to use to run the linter server. When set to `[]`, it will use the Python extension's selected interpreter. If set to some path, that path takes precedence, and the Python extension is not queried for the interpreter.|
|isort.importStrategy|`useBundled`|Setting to choose where to load `isort` from. `useBundled` picks isort bundled with the extension. `fromEnvironment` uses `isort` available in the environment.|
|isort.showNotification|`off`|Setting to control when a notification is shown.|
|isort.serverEnabled|`true`|**Experimental** setting to control running `isort` in a server like mode. By default we run `isort` behind LSP server, this setting allows users to turn off the server and run isort directly.|

## Commands

|Command|Description|
|---|---|
|isort: Restart|Force re-start the isort server.|

## Ведение журнала

Используйте `Developer : Set Log Level...` команду из **палитры команд** и выберите `isort` из списка расширений, чтобы установить уровень ведения журнала для расширения. Для получения подробных трассировок LSP добавьте их `"isort.trace.server" : "verbose"` в свой **пользовательский** `settings.json` файл.