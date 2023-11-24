[](https://github.com/israel-dryer/ttkbootstrap/edit/master/docs/styleguide/combobox.md "Редактировать эту страницу")

Этот стиль виджета содержит поле ввода со стилизованной рамкой и стрелкой. Цвет границы по умолчанию отключен и при **наведении** курсора мыши меняется на [основной](https://ttkbootstrap.readthedocs.io/en/latest/styleguide/#colors) или _выбранный цвет_. При _фокусировке_ толщина границы увеличивается. Цвет стрелки меняется на стандартный или [выбранный цвет](https://ttkbootstrap.readthedocs.io/en/latest/styleguide/#colors) при _наведении_ курсора или при _фокусировке_.

Этот виджет также поддерживает специальные стили для [отключенного состояния](https://ttkbootstrap.readthedocs.io/en/latest/styleguide/combobox/#disabled-combobox), [состояния только для чтения](https://ttkbootstrap.readthedocs.io/en/latest/styleguide/combobox/#readonly-combobox) и [недопустимого состояния](https://ttkbootstrap.readthedocs.io/en/latest/styleguide/combobox/#invalid-combobox).

![[Files/6ffaedee5689f66f8f3d2406f6e40837_MD5.gif]]

```
# default combobox style
Combobox()

# danger colored combobox style
Combobox(bootstyle="danger")

```

## Другие стили combobox

#### Отключен combobox

Этот стиль _нельзя применить с помощью ключевых слов_; он настраивается через настройки виджета.

```
# create the combobox in a disabled state
Combobox(state="disabled")

# disable a combobox after creation
cb = Combobox()
cb.configure(state="disabled")

```

#### combobox доступен только для чтения

Этот стиль _нельзя применить с помощью ключевых слов_; он настраивается через настройки виджета.

```
# create the combobox in a readonly state
Combobox(state="readonly")

# set the combobox readonly state after creation
cb = Combobox()
cb.configure(state="readonly")

```

#### Недопустимый combobox

Этот стиль _не может быть применен с помощью ключевых слов_, а скорее является результатом процесса проверки, реализованного в виджете. В **кулинарной книге** вы найдете пример того, [как применить проверку](https://ttkbootstrap.readthedocs.io/en/latest/cookbook/validate-user-input/) к `Entry` виджету на основе.