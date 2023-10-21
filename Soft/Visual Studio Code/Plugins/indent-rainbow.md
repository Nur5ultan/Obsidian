# Отступ-Rainbow

## Простое расширение, позволяющее сделать отступы более удобочитаемыми

Это расширение раскрашивает отступ перед вашим текстом, чередуя четыре разных цвета на каждом шаге. Некоторым это может оказаться полезным при написании кода для Python, Nim, Yaml и, возможно, даже для типов файлов, которые не зависят от отступа.

Примечание: Это также будет работать с vscode-web (github.dev) начиная с версии 8.0.0.

![[Files/78c40ee8f854b826a77ad6d3147958aa_MD5.png]]

Получить его можно здесь: [Visual Studio Code Marketplace](https://marketplace.visualstudio.com/items?itemName=oderwat.indent-rainbow)

Он использует текущий размер вкладки окна редактора и может обрабатывать сочетание табуляции и пробелов (не рекомендуется). Кроме того, он визуально отмечает строки, где отступ не кратен размеру вкладки. Визуализация может помочь в поиске проблем с отступом в некоторых ситуациях.

### Конфигурация

Хотя вы можете использовать его как есть, существует возможность настроить некоторые аспекты расширения:

```js
  // For which languages indent-rainbow should be activated (if empty it means all).
  "indentRainbow.includedLanguages": [] // for example ["nim", "nims", "python"]

  // For which languages indent-rainbow should be deactivated (if empty it means none).
  "indentRainbow.excludedLanguages": ["plaintext"]

  // The delay in ms until the editor gets updated.
  "indentRainbow.updateDelay": 100 // 10 makes it super fast but may cost more resources
```

_Обратите внимание: определение обоих `includedLanguages` и `excludedLanguages` не имеет особого смысла. Используйте одно из обоих!_

Вы можете настроить свои собственные цвета, добавив и изменив следующий код:

```js
  // Defining custom colors instead of default "Rainbow" for dark backgrounds.
  "indentRainbow.colors": [
    "rgba(255,255,64,0.07)",
    "rgba(127,255,127,0.07)",
    "rgba(255,127,255,0.07)",
    "rgba(79,236,236,0.07)"
  ]

  // The indent color if the number of spaces is not a multiple of "tabSize".
  "indentRainbow.errorColor": "rgba(128,32,32,0.6)"

  // The indent color when there is a mix between spaces and tabs.
  // To be disabled this coloring set this to an empty string.
  "indentRainbow.tabmixColor": "rgba(128,32,96,0.6)"
```

> Примечание: `errorColor` был переименован из `error_color` в более ранних версиях.

### Режим подсветки (новый с версии 8.3.0)

Существует (новый) альтернативный режим, который использует линии (с настраиваемой шириной) вместо фоновой раскраски пробела. Вот пример конфигурации, которая мне нравится:

```js
  // Using the light mode
  "indentRainbow.indicatorStyle": "light",
  // we use a simple 1 pixel wide line
  "indentRainbow.lightIndicatorStyleLineWidth": 1,
  // the same colors as above but more visible
  "indentRainbow.colors": [
    "rgba(255,255,64,0.3)",
    "rgba(127,255,127,0.3)",
    "rgba(255,127,255,0.3)",
    "rgba(79,236,236,0.3)"
```

> За это дополнение большое спасибо Кристиану Хоку [wk1](https://github.com/wk1). Он также добавил перезагрузку окна редактора при изменениях конфигурации.

### Hiding error highlighting

Пропустите выделение ошибок для шаблонов регулярных выражений. Например, вы можете отключить ошибки отступа для допустимого дополнительного пространства JSDoc (отключено по умолчанию) или строк комментариев, начинающихся с `//`

```js
  // Example of regular expression in JSON (note double backslash to escape characters)
  "indentRainbow.ignoreLinePatterns" : [
    "/[ \t]* [*]/g", // lines begining with <whitespace><space>*
    "/[ \t]+[/]{2}/g" // lines begininning with <whitespace>//
  ]
```

Пропустите выделение ошибок для некоторых или всех языков. Например, вы можете отключить ошибки отступа для `markdown` и `haskell` (которые используются по умолчанию).

```js
  "indentRainbow.ignoreErrorLanguages" : [
    "markdown",
    "haskell"
  ]
```

Если цвет ошибки отключен, цвета отступа будут отображаться до тех пор, пока длина отображаемых символов (пробелов, табуляции и других) не станет кратной размеру табуляции. Включите эту опцию для отображения только пробелов и табуляций.

```js
  "indentRainbow.colorOnWhiteSpaceOnly": true // false is the default
```

Сборка с помощью:

```
npm install
npm run vscode:prepublish
```

Запуск `npm run compile` приводит к перекомпиляции компилятора при изменении файла.