[](https://github.com/israel-dryer/ttkbootstrap/edit/master/docs/styleguide/spinbox.md "Редактировать эту страницу")

Этот стиль виджета включает в себя поле ввода со стилизованной рамкой и стрелками. Цвет границы по умолчанию отключен и меняется на **основной** или [выбранный цвет](https://ttkbootstrap.readthedocs.io/en/latest/styleguide/#colors) при _наведении_ курсора. При _фокусировке_ толщина рамки увеличивается. Цвет стрелки меняется на стандартный или [выбранный цвет](https://ttkbootstrap.readthedocs.io/en/latest/styleguide/#colors) при _наведении_ курсора или при _фокусировке_.

Этот виджет также поддерживает специальные стили для [отключенного состояния](https://ttkbootstrap.readthedocs.io/en/latest/styleguide/spinbox/#disabled-spinbox), [состояния только для чтения](https://ttkbootstrap.readthedocs.io/en/latest/styleguide/spinbox/#readonly-spinbox) и [недопустимого состояния](https://ttkbootstrap.readthedocs.io/en/latest/styleguide/spinbox/#invalid-combobox).

![[Files/90d8f9a2043d63914383c41351f3d397_MD5.gif]]

```
# default spinbox style
Spinbox()

# danger colored spinbox style
Spinbox(bootstyle="danger")

```

## Другие стили

#### Отключен spinbox

Этот виджет поддерживает стиль, зарезервированный для **отключенного** состояния, который вы можете увидеть на рисунке выше. Этот стиль _нельзя применить с помощью ключевых слов_. Чтобы применить отключенный стиль:

```
# create the widget in a disabled state
Spinbox(state="disabled")

# disable the widget after creation
e = Spinbox()
e.configure(state="disabled")

```

#### spinbox доступен только для чтения

Этот виджет поддерживает стиль, зарезервированный для состояния **только для чтения**, который вы можете увидеть на рисунке выше. Этот стиль _нельзя применить с помощью ключевых слов_. Чтобы применить стиль только для чтения:

```
# create the widget in a readonly state
Spinbox(state="readonly")

# set the widget readonly state after creation
e = Spinbox()
e.configure(state="readonly")

```

#### Недопустимый spinbox

Этот стиль _не может быть применен с помощью ключевых слов_, а скорее является результатом процесса проверки, реализованного в виджете. В **Кулинарной книге** вы найдете пример того, [как применить проверку](https://ttkbootstrap.readthedocs.io/en/latest/cookbook/validate-user-input/) к виджету на `Entry` основе.