[](https://github.com/israel-dryer/ttkbootstrap/edit/master/docs/styleguide/scale.md "Отредактируйте эту страницу")

## Масштабирование

Этот стиль виджета имеет тонкую серую рамку с круглой ручкой-ползунком, которая является **основным** цветом по умолчанию или [выбранным цветом](https://ttkbootstrap.readthedocs.io/en/latest/styleguide/#colors). Ручка ползунка светлеет при _наведении_ курсора мыши и темнеет при _нажатии_.

Этот виджет поддерживает специальный стиль для [отключенного состояния](https://ttkbootstrap.readthedocs.io/en/latest/styleguide/scale/#other-scale-styles).

![[Files/9ecee9d635846b9c33e64d466c078668_MD5.gif]]

```
# default Scale style
Scale()

# info colored label style
Scale(bootstyle="info")

```

## Другие стили масштабирования

#### Отключено масштабирование

Этот стиль _нельзя применить с помощью ключевых слов_; он настраивается через настройки виджета.

```
# create the scale in a disabled state
Scale(state="disabled")

# disable a scale after creation
scale = Scale()
scale.configure(state="disabled")

```