[](https://github.com/israel-dryer/ttkbootstrap/edit/master/docs/styleguide/progressbar.md "Отредактируйте эту страницу")

## Панель прогресса

Этот виджет имеет несколько типов стилей, которые по умолчанию имеют **основные** цветные индикаторные полосы, но могут быть стилизованы с использованием любого из [доступных цветов](https://ttkbootstrap.readthedocs.io/en/latest/styleguide/#colors).

## Сплошной (по умолчанию)

Стиль виджета по умолчанию имеет сплошную цветную индикаторную панель.

![[Files/94b632c8fd3f0bff24e6df8cdcbbd033_MD5.gif]]

```
# default solid progressbar style
Progressbar()

# success colored solid progressbar style
Progressbar(bootstyle="success")

```

## Полосатая

Этот стиль виджета включает полосатую индикаторную полосу, которая использует цвет по умолчанию или [выбранный цвет](https://ttkbootstrap.readthedocs.io/en/latest/styleguide/#colors) в качестве основного цвета, и ненасыщенную версию этого цвета для чередующейся полосы.

![[Files/8d9cb4706a9944c18dc842ef2a95343d_MD5.gif]]

```
# default striped progressbar style
Progressbar(bootstyle="striped")

# danger colored striped progressbar style
Progressbar(bootstyle="danger-striped")

```