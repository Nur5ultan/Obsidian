[](https://github.com/israel-dryer/ttkbootstrap/edit/master/docs/styleguide/entry.md "Редактировать эту страницу")

## Запись

Этот стиль виджета содержит поле ввода со стилизованной рамкой. Цвет границы по умолчанию отключен и меняется на **основной** или [выбранный цвет](https://ttkbootstrap.readthedocs.io/en/latest/styleguide/#colors) при _наведении_ курсора мыши. При _фокусировке_ толщина границы увеличивается.

Этот виджет также поддерживает специальные стили для [отключенного состояния](https://ttkbootstrap.readthedocs.io/en/latest/styleguide/entry/#disabled-entry), [состояния только для чтения](https://ttkbootstrap.readthedocs.io/en/latest/styleguide/entry/#readonly-entry) и [недопустимого состояния](https://ttkbootstrap.readthedocs.io/en/latest/styleguide/entry/#invalid-entry).

![запись](https://ttkbootstrap.readthedocs.io/en/latest/assets/widget-styles/entries.gif)

```
# default entry style
Entry()

# danger colored entry style
Entry(bootstyle="danger")

```

## Другие стили записи

#### Запись отключена

Этот стиль _не может быть применен с помощью ключевых слов_; он настраивается через настройки виджета.

```
# create the widget in a disabled state
Entry(state="disabled")

# disable the widget after creation
e = Entry()
e.configure(state="disabled")

```

#### Запись только для чтения

Этот стиль _не может быть применен с помощью ключевых слов_; он настраивается через настройки виджета.

```
# create the widget in a readonly state
Entry(state="readonly")

# set the widget readonly state after creation
e = Entry()
e.configure(state="readonly")

```

#### Недопустимая запись

Этот стиль _не может быть применен с помощью ключевых слов_, а скорее является результатом процесса проверки, реализованного в виджете. В **Кулинарной книге** вы найдете пример того, [как применить проверку](https://ttkbootstrap.readthedocs.io/en/latest/cookbook/validate-user-input/) к виджету на `Entry` основе.