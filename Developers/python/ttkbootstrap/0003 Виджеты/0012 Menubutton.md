[](https://github.com/israel-dryer/ttkbootstrap/edit/master/docs/styleguide/menubutton.md "Редактировать эту страницу")

Этот виджет имеет стильную кнопку со стрелкой, которую можно оформить любым из [доступных цветов](https://ttkbootstrap.readthedocs.io/en/latest/styleguide/#colors).

Этот виджет поддерживает специальный стиль для [отключенного состояния](https://ttkbootstrap.readthedocs.io/en/latest/styleguide/menubutton/#disabled-menubutton).

## Твердотельный (по умолчанию)

Этот стиль виджета имеет сплошной цвет фона, который светлеет при _наведении_ курсора мыши и темнеет при _нажатии_.

![[Files/6c2d9afc8027276c0c39b873d990fff7_MD5.gif]]

```
# default solid menubutton style
Menubutton()

# success colored solid menubutton style
Menubutton(bootstyle="success")

```

## Схема

Этот стиль отличается тонким стилизованным контуром. При _нажатии_ или при _наведении_ курсора мыши кнопка приобретает сплошной цвет, аналогичный стилю menubutton по умолчанию.

![[Files/a708bca1e3465b704b3dd1bfc9edc11d_MD5.gif]]

```
# default outline menubutton style
Menubutton(bootstyle="outline")

# info colored outline menubutton style
Menubutton(bootstyle="info-outline")

```

Этот стиль _нельзя применить с помощью ключевых слов_; он настраивается через настройки виджета.

```
# create the menubutton in a disabled state
Menubutton(state="disabled")

# disable a menubutton after creation
b = Menubutton()
b.configure(state="disabled")

```