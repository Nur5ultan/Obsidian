Расширение Better Comments поможет вам создавать более понятные для пользователя комментарии в вашем коде.  
С помощью этого расширения вы сможете классифицировать свои аннотации на:

- Оповещения
- Запросы
- TODOs
- Основные моменты
- Закомментированный код также можно оформить так, чтобы было ясно, что кода там быть не должно
- Любые другие желаемые стили комментариев можно указать в настройках

![[Files/770622a662bee5822341898480b61726_MD5.png]]

## Конфигурация

Это расширение можно настроить в настройках пользователя или рабочей области.

`"better-comments.multilineComments": true`  
Этот параметр определяет, будут ли многострочные комментарии оформлены с использованием тегов аннотаций. При значении false многострочные комментарии будут представлены без оформления.

`"better-comments.highlightPlainText": false`  
Этот параметр определяет, будут ли комментарии в обычном текстовом файле оформлены с использованием тегов аннотаций. При значении true теги (по умолчанию: `! * ? //`) будут обнаружены, если они являются первым символом в строке.

`better-comments.tags`  
Теги - это символы или последовательности, используемые для обозначения комментария для оформления. Значения по умолчанию 5 могут быть изменены для изменения цветов, а также могут быть добавлены дополнительные.

```json
"better-comments.tags": [
  {
    "tag": "!",
    "color": "#FF2D00",
    "strikethrough": false,
    "underline": false,
    "backgroundColor": "transparent",
    "bold": false,
    "italic": false
  },
  {
    "tag": "?",
    "color": "#3498DB",
    "strikethrough": false,
    "underline": false,
    "backgroundColor": "transparent",
    "bold": false,
    "italic": false
  },
  {
    "tag": "//",
    "color": "#474747",
    "strikethrough": true,
    "underline": false,
    "backgroundColor": "transparent",
    "bold": false,
    "italic": false
  },
  {
    "tag": "todo",
    "color": "#FF8C00",
    "strikethrough": false,
    "underline": false,
    "backgroundColor": "transparent",
    "bold": false,
    "italic": false
  },
  {
    "tag": "*",
    "color": "#98C379",
    "strikethrough": false,
    "underline": false,
    "backgroundColor": "transparent",
    "bold": false,
    "italic": false
  }
]
```

## Поддерживаемые языки
- Ada
- AL
- Apex
- AsciiDoc
- BrightScript
- C
- C#
- C++
- ColdFusion
- Clojure
- COBOL
- CoffeeScript
- CSS
- Dart
- Dockerfile
- Elixir
- Elm
- Erlang
- F#
- Fortran
- gdscript
- GenStat
- Go
- GraphQL
- Groovy
- Haskell
- Haxe
- HiveQL
- HTML
- Java
- JavaScript
- JavaScript React
- JSON with comments
- Julia
- Kotlin
- LaTex (inlc. Bibtex/Biblatex)
- Less
- Lisp
- Lua
- Makefile
- Markdown
- Nim
- MATLAB
- Objective-C
- Objective-C++
- Pascal
- Perl
- Perl 6
- PHP
- Pig
- PlantUML
- PL/SQL
- PowerShell
- Puppet
- Python
- R
- Racket
- Ruby
- Rust
- SAS
- Sass
- Scala
- SCSS
- ShaderLab
- ShellScript
- SQL
- STATA
- Stylus
- Svelte
- Swift
- Tcl
- Terraform
- Twig
- TypeScript
- TypeScript React
- Verilog
- Visual Basic
- Vue.js
- XML
- YAML