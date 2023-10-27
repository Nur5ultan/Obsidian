[](https://github.com/israel-dryer/ttkbootstrap/edit/master/docs/styleguide/dateentry.md "Редактировать эту страницу")

## Ввод данных

Этот виджет состоит из двух виджетов: виджета "**Запись**" и виджета "**Кнопка**". На **вход** компонент ведет себя одинаково к [умолчанию входа виджет](https://ttkbootstrap.readthedocs.io/en/latest/styleguide/entry/), и календарь, кнопка ведет себя как [по умолчанию прочную кнопку](https://ttkbootstrap.readthedocs.io/en/latest/styleguide/button/).

При нажатии кнопки календаря вызывается [DatePickerPopup](https://ttkbootstrap.readthedocs.io/en/latest/styleguide/datepickerpopup/). Цвет по умолчанию, применяемый к всплывающему окну, является **основным**.

Этот виджет также поддерживает специальные стили для [отключенного состояния](https://ttkbootstrap.readthedocs.io/en/latest/styleguide/dateentry/#disabled-date-entry), [состояния только для чтения](https://ttkbootstrap.readthedocs.io/en/latest/styleguide/dateentry/#readonly-date-entry) и [недопустимого состояния](https://ttkbootstrap.readthedocs.io/en/latest/styleguide/dateentry/#invalid-date-entry).

![[Files/e463506c41e6b28e06cecd28586cea3d_MD5.gif]]

```
# default date entry
DateEntry()

# success colored date entry
DateEntry(bootstyle="success")

```

## Другие стили ввода даты

#### Отключен ввод даты

Этот стиль _не может быть применен с помощью ключевых слов_; он настраивается с помощью настроек виджета.

```
# create the date entry in a disabled state
DateEntry(state="disabled")

# disable a date entry after creation
d = DateEntry()
d.configure(state="disabled")

```

#### Ввод даты только для чтения

Этот стиль _не может быть применен с помощью ключевых слов_; он настраивается с помощью настроек виджета.

```
# create the date entry in a readonly state
DateEntry(state="readonly")

# set the date entry readonly state after creation
d = DateEntry()
d.configure(state="readonly")

```

#### Неверный ввод даты

Этот стиль _не может быть применен с помощью ключевых слов_, а скорее является результатом процесса проверки, реализованного в виджете. В **кулинарной книге** вы найдете пример того, [как применить проверку](https://ttkbootstrap.readthedocs.io/en/latest/cookbook/validate-user-input/) к `Entry` виджету на основе.