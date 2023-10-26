[](https://github.com/israel-dryer/ttkbootstrap/edit/master/docs/styleguide/radiobutton.md "Редактировать эту страницу")

## Радиокнопка

В этом виджете представлены различные типы стилей radiobutton, которые по умолчанию имеют **основной** цвет или [выбранный цвет](https://ttkbootstrap.readthedocs.io/en/latest/styleguide/#colors).

Этот виджет поддерживает специальный стиль для [отключенного состояния](https://ttkbootstrap.readthedocs.io/en/latest/styleguide/radiobutton/#other-radiobutton-styles).

## Радио (по умолчанию)

Стиль виджета по умолчанию использует традиционную **radiobutton** с круглым индикатором. Индикатор заливается цветом по умолчанию или выбранным цветом, когда находится в _выбранном состоянии_.

![[Files/9da47d41ebf2a69716f6f44c78dc7318_MD5.png]]

```
# default radiobutton style
Radiobutton()

# secondary colored radiobutton style
Radiobutton(bootstyle="secondary")

```

В этом стиле используется сплошная прямоугольная кнопка, которая имеет приглушенный серый фон, если она _не выбрана_, и цвет по умолчанию или [выбранный цвет](https://ttkbootstrap.readthedocs.io/en/latest/styleguide/#colors), если она _выбрана_ или _активна_.

![[Files/d933760606dfc8a8477b8c203c4ab587_MD5.gif]]

```
# default toolbutton style
Radiobutton(bootstyle="toolbutton")

# danger colored radio toolbutton style
Radiobutton(bootstyle="danger-toolbutton")

```

В этом стиле используется прямоугольная кнопка, которая имеет **контур**, когда она _не выбрана_, и **сплошной** фон, когда она _выбрана_ или _активна_.

![[Files/a8ada8601e65489bba044a42a4c7e8a2_MD5.gif]]

```
# default outline radio toolbutton style
Radiobutton(bootstyle="outline-toolbutton")

# info colored outline radio toolbutton style
Radiobutton(bootstyle="info-outline-toolbutton")

```

#### Отключена radiobutton

Этот стиль _нельзя применить с помощью ключевых слов_; он настраивается через настройки виджета.

```
# create the radiobutton in a disabled state
Radiobutton(state="disabled")

# disable a radiobutton after creation
rb = Radiobutton()
rb.configure(state="disabled")

```