[](https://github.com/israel-dryer/ttkbootstrap/edit/master/docs/styleguide/scrollbar.md "Отредактируйте эту страницу")

Этот стиль виджета имеет светло-серый желоб с кнопками в виде большого пальца и стрелок. Большой палец и стрелки становятся светлее при _наведении_ курсора мыши и темнеют при _нажатии_. Большой палец и стрелки могут быть выполнены в любом из [доступных цветов](https://ttkbootstrap.readthedocs.io/en/latest/styleguide/#colors).

## Квадратная (по умолчанию)

Стиль по умолчанию представляет собой большой палец с квадратными краями.

![[Files/1f61fba5c80b9d99a071a8ae0d10dfa6_MD5.png]]

```
# default scrollbar style
Scrollbar()

# success colored default scrollbar style
Scrollbar(bootstyle="success")

```

## Круглая

В **круглом** стиле используется большой палец со скругленными краями.

![[Files/c4667cc6e86ea933f5d5dc0fa7928167_MD5.png]]

```
# default round scrollbar style
Scrollbar(bootstyle="round")

# danger colored round scrollbar style
Scrollbar(bootstyle="danger-round")

```