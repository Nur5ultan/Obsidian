Настройки для программы VS Code. Которые записываются в файле **settings.json**

```json
{

  "editor.cursorStyle": "line-thin", // Стиль курсора

  "editor.cursorBlinking": "expand", // Стиль анимации курсора

  "editor.cursorSmoothCaretAnimation": "on", // Плавная анимация курсора

  "terminal.integrated.cursorStyle": "line", // Стиль курсора

  "terminal.integrated.cursorBlinking": true, // Мигающий курсор

  "terminal.integrated.cursorStyleInactive": "line", // Стиль курсора, когда терминал неактивен

  "terminal.integrated.cursorWidth": 2.4, // Ширина курсора

  "editor.defaultFormatter": "esbenp.prettier-vscode",

  "editor.fontLigatures": true, // Отображение лигатуры

  "editor.formatOnPaste": true, // Автоматическое форматирование при вставке

  "editor.formatOnSave": true, // Форматирование при сохранений

  "editor.formatOnType": true, // Форматировать строку при вводе

  "editor.minimap.enabled": false, // Отключить мини-карту

  "editor.wordWrap": "on", // Включение переноса строк

  "files.autoSave": "afterDelay", // Файлы автоматически сохраняются после некоторой задержки.

  "files.trimFinalNewlines": true, // Удаление пустых строк в конце файла

  "terminal.integrated.defaultProfile.windows": "Command Prompt", // Терминал по умолчанию CMD

  "workbench.startupEditor": "none", // Отключение окна приветствия

  "workbench.colorTheme": "Bluloco Dark Italic", // тема vs code

  "workbench.iconTheme": "material-icon-theme", // иконки файлов и папок

  "security.workspace.trust.startupPrompt": "never", // Не запрашивает доверие при открытии проектов

  "security.workspace.trust.enabled": false, // Включено или отключено доверие в рабочей области

  "security.workspace.trust.banner": "never", // Не показывает баннер при открытии не доверенных проектов

  "security.workspace.trust.emptyWindow": false, // Определяет при открытии пустого окна, доверенное ли оно

  // Python

  "python.analysis.inlayHints.variableTypes": true, // показывает типы

  "python.analysis.inlayHints.functionReturnTypes": true, // показывает какие типы будут возвращены

  "[python]": {

    "editor.formatOnType": true, // Форматирование кода при вводе для языка Python

    "editor.defaultFormatter": "ms-python.black-formatter" // Использование автоформатера autopep8 для Python

  },

  // Code Spell Checker

  "cSpell.language": "en, ru",

  "cSpell.userWords": ["автоформатера", "autopep", "Bluloco", "esbenp"],

  

  // Code Runner

  "code-runner.clearPreviousOutput": true,

  "code-runner.runInTerminal": true // Запуск кода в терминале

}
```

