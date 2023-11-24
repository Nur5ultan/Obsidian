[](https://github.com/israel-dryer/ttkbootstrap/edit/master/docs/styleguide/checkbutton.md "Редактировать эту страницу")

## Кнопка проверки

Этот виджет содержит множество типов стилей checkbutton, которые по умолчанию имеют **основной** цвет или [выбранный цвет](https://ttkbootstrap.readthedocs.io/en/latest/styleguide/#colors).

Этот виджет поддерживает специальный стиль для [отключенного состояния](https://ttkbootstrap.readthedocs.io/en/latest/styleguide/checkbutton/#other-checkbutton-styles).

Стиль по умолчанию включает квадратный флажок и надпись. Флажок имеет контур приглушенного цвета, если он не установлен, и заполненный квадрат с галочкой, если он установлен.

![[Files/de15f6532e38dacf175e4af953b0b154_MD5.webp]]

```
# default checkbutton style
Checkbutton()

# success checkbutton style
Checkbutton(bootstyle="success")

```

В этом стиле используется сплошная прямоугольная кнопка, которая переключает между _выкл_ и _включенным_ цветом. Фон имеет приглушенный серый цвет, когда он _выключен_, и цвет по умолчанию или [выбранный](https://ttkbootstrap.readthedocs.io/en/latest/styleguide/#colors), когда он _включен_ или _активен_.

![[Files/2c7d1e822eb53aab745c1557fec7be2b_MD5.gif]]

```
# default toolbutton style
Checkbutton(bootstyle="toolbutton")

# success toolbutton style
Checkbutton(bootstyle="success-toolbutton")

```

В этом стиле используется прямоугольная кнопка, которая переключается между стилизованным **контуром**, когда он _выключен_, и **сплошным** фоном, когда он _включен_ или _активен_.

![[Files/7c9659399fa4a9d1e23e7f554813e5d9_MD5.gif]]

```
# default outline toolbutton style
Checkbutton(bootstyle="outline-toolbutton")

# success outline toolbutton style
Checkbutton(bootstyle="success-outline-toolbutton")

```

## Круглая кнопка переключения

В этом стиле используется закругленная кнопка с **круглым** индикатором, который меняет цвет и положение при _выключении_ и _включении_. Кнопка имеет приглушенный контур с индикатором приглушенного цвета, когда _выключена_. Кнопка заполняется цветом по умолчанию или [выбранным цветом](https://ttkbootstrap.readthedocs.io/en/latest/styleguide/#colors) с выделенным индикатором, когда _включена_.

![[Files/b926930a65a2d9ee2a34387e68c5f21a_MD5.gif]]

```
# default round toggle style
Checkbutton(bootstyle="round-toggle")

# success round toggle style
Checkbutton(bootstyle="success-round-toggle")

```

## Квадратная кнопка переключения

В этом стиле используется квадратная кнопка с **квадратным** индикатором, который меняет цвет и положение при _выключении_ и _включении_. Кнопка имеет приглушенный контур с индикатором приглушенного цвета, когда _выключена_. Кнопка заполняется цветом по умолчанию или [выбранным цветом](https://ttkbootstrap.readthedocs.io/en/latest/styleguide/#colors) с выделенным индикатором, когда _включена_.

![[Files/5966c5898c0b95cb42f13c56fd3d51e9_MD5.gif]]

```
# default square toggle style
Checkbutton(bootstyle="square-toggle")

# success square toggle style
Checkbutton(bootstyle="success-square-toggle")

```

## Другие стили checkbutton

#### Отключена checkbutton

Этот стиль _нельзя применить с помощью ключевых слов_; он настраивается через настройки виджета.

```
# create the checkbutton in a disabled state
Checkbutton(state="disabled")

# disable a checkbutton after creation
cb = Checkbutton()
cb.configure(state="disabled")

```