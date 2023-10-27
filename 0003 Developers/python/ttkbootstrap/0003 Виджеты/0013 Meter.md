[](https://github.com/israel-dryer/ttkbootstrap/edit/master/docs/styleguide/meter.md "Отредактируйте эту страницу")

## Измеритель

Этот стиль виджета включает в себя набор компонентов. Индикатор и основная метка являются **основными** по умолчанию или имеют [выбранный цвет](https://ttkbootstrap.readthedocs.io/en/latest/styleguide/#colors). Если указано, подтекст-это **среднее** для светлой темы и **свет** для темной темы. Однако все эти элементы можно настроить, используя [доступные цвета](https://ttkbootstrap.readthedocs.io/en/latest/styleguide/#colors).

![[Files/97d26b647c406180cea4214792f6cfd8_MD5.gif]]

Виджет счетчика легко настраивается и может создавать разнообразные интересные счетчики путем смешивания цветов и других настроек, специфичных для виджета.

![[Files/0195ecdd5a817dacfabe8889df49144f_MD5.png]]

```
# default meter style
Meter()

# info colored meter
Meter(bootstyle="info")

# danger color subtext
Meter(subtextstyle="danger")

# success colored meter with warning colored subtext
Meter(bootstyle="success", subtextstyle="warning")

```