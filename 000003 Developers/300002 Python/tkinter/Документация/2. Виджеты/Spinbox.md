Виджет Spinbox позволяет выбрать значение (чаще число) из некоторого списка.

Основные параметры Spinbox:

-   values: набор значений виджета в виде списка или кортежа
    
-   from\_: минимальное значение (тип float)
    
-   to: максимальное значение (тип float)
    
-   increment: приращение значения (тип float)
    
-   textvariable: определяет переменную StringVar, которая хранит текущее значение виджета
    
-   command: указывает на функцию, которая вызывается при изменении значения виджета
    
-   wrap: при значении True создает зацикленный список, при котором после минимального значения идет максимальное.
    
-   background: фоновый цвет
    
-   foreground: цвет текста
    
-   font: шрифт виджета
    
-   justify: выравнивание текста, принимает значения "left" (по левому краю), "right" (по правому краю) и "center" (по центру)
    
-   width: ширина виджета
    
-   state: состояние виджета
    

Простейший Spinbox:

[?](https://metanit.com/python/tkinter/2.16.php#)

<table border="0" cellpadding="0" cellspacing="0"><tbody><tr><td class="gutter"><div class="line number1 index0 alt2">1</div><div class="line number2 index1 alt1">2</div><div class="line number3 index2 alt2">3</div><div class="line number4 index3 alt1">4</div><div class="line number5 index4 alt2">5</div><div class="line number6 index5 alt1">6</div><div class="line number7 index6 alt2">7</div><div class="line number8 index7 alt1">8</div><div class="line number9 index8 alt2">9</div><div class="line number10 index9 alt1">10</div><div class="line number11 index10 alt2">11</div></td><td class="code"><div class="container"><div class="line number1 index0 alt2"><code class="py keyword">from</code> <code class="py plain">tkinter </code><code class="py keyword">import</code> <code class="py keyword">*</code></div><div class="line number2 index1 alt1"><code class="py keyword">from</code> <code class="py plain">tkinter </code><code class="py keyword">import</code> <code class="py plain">ttk</code></div><div class="line number3 index2 alt2">&nbsp;</div><div class="line number4 index3 alt1"><code class="py plain">root </code><code class="py keyword">=</code> <code class="py plain">Tk()</code></div><div class="line number5 index4 alt2"><code class="py plain">root.title(</code><code class="py string">"METANIT.COM"</code><code class="py plain">)</code></div><div class="line number6 index5 alt1"><code class="py plain">root.geometry(</code><code class="py string">"250x200"</code><code class="py plain">)</code></div><div class="line number7 index6 alt2">&nbsp;</div><div class="line number8 index7 alt1"><code class="py plain">spinbox </code><code class="py keyword">=</code> <code class="py plain">ttk.Spinbox(from_</code><code class="py keyword">=</code><code class="py value">1.0</code><code class="py plain">, to</code><code class="py keyword">=</code><code class="py value">100.0</code><code class="py plain">)</code></div><div class="line number9 index8 alt2"><code class="py plain">spinbox.pack(anchor</code><code class="py keyword">=</code><code class="py plain">NW)</code></div><div class="line number10 index9 alt1">&nbsp;</div><div class="line number11 index10 alt2"><code class="py plain">root.mainloop()</code></div></div></td></tr></tbody></table>

В данном случае мы можем выбрать одно из чисел от 1 до 100. При нажатии на стрелочки вверх и вниз на виджете значение виджета будет увелиличивается и уменьшаться на единицу:

![Spinbox в Tkinter и Python](https://metanit.com/python/tkinter/2.16.php./pics/2.73.png)

По умолчанию приращение идет на единицу, но с помощью параметра increment можно установить другое значение, например, приращение на 2:

[?](https://metanit.com/python/tkinter/2.16.php#)

<table border="0" cellpadding="0" cellspacing="0"><tbody><tr><td class="gutter"><div class="line number1 index0 alt2">1</div></td><td class="code"><div class="container"><div class="line number1 index0 alt2"><code class="py plain">ttk.Spinbox(from_</code><code class="py keyword">=</code><code class="py value">1.0</code><code class="py plain">, to</code><code class="py keyword">=</code><code class="py value">100.0</code><code class="py plain">, increment</code><code class="py keyword">=</code><code class="py value">2</code><code class="py plain">)</code></div></div></td></tr></tbody></table>

Также по умолчанию мы можем, не используя стрелочки, ввести в текстовое поле виджета какое-либо значение, даже то, которое не входит в диапазон значений. Если нам надо запретить ввод значений в текстовое поле и оставить доступными для выбора значений только стрелочки, то для этого можно установить для параметра `state` значение `readonly`:

[?](https://metanit.com/python/tkinter/2.16.php#)

<table border="0" cellpadding="0" cellspacing="0"><tbody><tr><td class="gutter"><div class="line number1 index0 alt2">1</div></td><td class="code"><div class="container"><div class="line number1 index0 alt2"><code class="py plain">spinbox </code><code class="py keyword">=</code> <code class="py plain">ttk.Spinbox(from_</code><code class="py keyword">=</code><code class="py value">1.0</code><code class="py plain">, to</code><code class="py keyword">=</code><code class="py value">100.0</code><code class="py plain">, state</code><code class="py keyword">=</code><code class="py string">"readonly"</code><code class="py plain">)</code></div></div></td></tr></tbody></table>

С помощью параметра textvariable можно привязать значение Spinbox к переменной StringVar:

[?](https://metanit.com/python/tkinter/2.16.php#)

<table border="0" cellpadding="0" cellspacing="0"><tbody><tr><td class="gutter"><div class="line number1 index0 alt2">1</div><div class="line number2 index1 alt1">2</div><div class="line number3 index2 alt2">3</div><div class="line number4 index3 alt1">4</div><div class="line number5 index4 alt2">5</div><div class="line number6 index5 alt1">6</div><div class="line number7 index6 alt2">7</div><div class="line number8 index7 alt1">8</div><div class="line number9 index8 alt2">9</div><div class="line number10 index9 alt1">10</div><div class="line number11 index10 alt2">11</div><div class="line number12 index11 alt1">12</div><div class="line number13 index12 alt2">13</div><div class="line number14 index13 alt1">14</div><div class="line number15 index14 alt2">15</div><div class="line number16 index15 alt1">16</div></td><td class="code"><div class="container"><div class="line number1 index0 alt2"><code class="py keyword">from</code> <code class="py plain">tkinter </code><code class="py keyword">import</code> <code class="py keyword">*</code></div><div class="line number2 index1 alt1"><code class="py keyword">from</code> <code class="py plain">tkinter </code><code class="py keyword">import</code> <code class="py plain">ttk</code></div><div class="line number3 index2 alt2">&nbsp;</div><div class="line number4 index3 alt1"><code class="py plain">root </code><code class="py keyword">=</code> <code class="py plain">Tk()</code></div><div class="line number5 index4 alt2"><code class="py plain">root.title(</code><code class="py string">"METANIT.COM"</code><code class="py plain">)</code></div><div class="line number6 index5 alt1"><code class="py plain">root.geometry(</code><code class="py string">"250x150"</code><code class="py plain">)</code></div><div class="line number7 index6 alt2">&nbsp;</div><div class="line number8 index7 alt1"><code class="py plain">spinbox_var </code><code class="py keyword">=</code> <code class="py plain">StringVar(value</code><code class="py keyword">=</code><code class="py value">22</code><code class="py plain">) </code><code class="py comments"># начальное значение 22</code></div><div class="line number9 index8 alt2">&nbsp;</div><div class="line number10 index9 alt1"><code class="py plain">label </code><code class="py keyword">=</code> <code class="py plain">ttk.Label(textvariable</code><code class="py keyword">=</code><code class="py plain">spinbox_var)</code></div><div class="line number11 index10 alt2"><code class="py plain">label.pack(anchor</code><code class="py keyword">=</code><code class="py plain">NW)</code></div><div class="line number12 index11 alt1">&nbsp;</div><div class="line number13 index12 alt2"><code class="py plain">spinbox </code><code class="py keyword">=</code> <code class="py plain">ttk.Spinbox(from_</code><code class="py keyword">=</code><code class="py value">1.0</code><code class="py plain">, to</code><code class="py keyword">=</code><code class="py value">100.0</code><code class="py plain">, textvariable</code><code class="py keyword">=</code><code class="py plain">spinbox_var)</code></div><div class="line number14 index13 alt1"><code class="py plain">spinbox.pack(anchor</code><code class="py keyword">=</code><code class="py plain">NW)</code></div><div class="line number15 index14 alt2">&nbsp;</div><div class="line number16 index15 alt1"><code class="py plain">root.mainloop()</code></div></div></td></tr></tbody></table>

Здесь для наглядности добавлена метка, которая выводит выбранное значение. В качестве начального значения применяется число 22.

![Spinbox и привязка к переменной StringVar в Tkinter и Python](https://metanit.com/python/tkinter/2.16.php./pics/2.74.png)

### Получение текущего значения

Для получения текущего значения у Spinbox вызывается метод get()

[?](https://metanit.com/python/tkinter/2.16.php#)

<table border="0" cellpadding="0" cellspacing="0"><tbody><tr><td class="gutter"><div class="line number1 index0 alt2">1</div></td><td class="code"><div class="container"><div class="line number1 index0 alt2"><code class="py plain">current_value </code><code class="py keyword">=</code> <code class="py plain">spinbox.get()</code></div></div></td></tr></tbody></table>

### Обработка изменения значения

Чтобы обработать изменение значения нужно определить функцию, которая будет срабатывать при изменении значения, и передать ее параметру command:

[?](https://metanit.com/python/tkinter/2.16.php#)

<table border="0" cellpadding="0" cellspacing="0"><tbody><tr><td class="gutter"><div class="line number1 index0 alt2">1</div><div class="line number2 index1 alt1">2</div><div class="line number3 index2 alt2">3</div><div class="line number4 index3 alt1">4</div><div class="line number5 index4 alt2">5</div><div class="line number6 index5 alt1">6</div><div class="line number7 index6 alt2">7</div><div class="line number8 index7 alt1">8</div><div class="line number9 index8 alt2">9</div><div class="line number10 index9 alt1">10</div><div class="line number11 index10 alt2">11</div><div class="line number12 index11 alt1">12</div><div class="line number13 index12 alt2">13</div><div class="line number14 index13 alt1">14</div><div class="line number15 index14 alt2">15</div><div class="line number16 index15 alt1">16</div><div class="line number17 index16 alt2">17</div></td><td class="code"><div class="container"><div class="line number1 index0 alt2"><code class="py keyword">from</code> <code class="py plain">tkinter </code><code class="py keyword">import</code> <code class="py keyword">*</code></div><div class="line number2 index1 alt1"><code class="py keyword">from</code> <code class="py plain">tkinter </code><code class="py keyword">import</code> <code class="py plain">ttk</code></div><div class="line number3 index2 alt2">&nbsp;</div><div class="line number4 index3 alt1"><code class="py plain">root </code><code class="py keyword">=</code> <code class="py plain">Tk()</code></div><div class="line number5 index4 alt2"><code class="py plain">root.title(</code><code class="py string">"METANIT.COM"</code><code class="py plain">)</code></div><div class="line number6 index5 alt1"><code class="py plain">root.geometry(</code><code class="py string">"250x200"</code><code class="py plain">)</code></div><div class="line number7 index6 alt2">&nbsp;</div><div class="line number8 index7 alt1"><code class="py keyword">def</code> <code class="py plain">change():</code></div><div class="line number9 index8 alt2"><code class="py spaces">&nbsp;&nbsp;&nbsp;&nbsp;</code><code class="py plain">label[</code><code class="py string">"text"</code><code class="py plain">] </code><code class="py keyword">=</code> <code class="py plain">spinbox.get()</code></div><div class="line number10 index9 alt1">&nbsp;</div><div class="line number11 index10 alt2"><code class="py plain">label </code><code class="py keyword">=</code> <code class="py plain">ttk.Label()</code></div><div class="line number12 index11 alt1"><code class="py plain">label.pack(anchor</code><code class="py keyword">=</code><code class="py plain">NW)</code></div><div class="line number13 index12 alt2">&nbsp;</div><div class="line number14 index13 alt1"><code class="py plain">spinbox </code><code class="py keyword">=</code> <code class="py plain">ttk.Spinbox(from_</code><code class="py keyword">=</code><code class="py value">1.0</code><code class="py plain">, to</code><code class="py keyword">=</code><code class="py value">100.0</code><code class="py plain">, command</code><code class="py keyword">=</code><code class="py plain">change)</code></div><div class="line number15 index14 alt2"><code class="py plain">spinbox.pack(anchor</code><code class="py keyword">=</code><code class="py plain">NW)</code></div><div class="line number16 index15 alt1">&nbsp;</div><div class="line number17 index16 alt2"><code class="py plain">root.mainloop()</code></div></div></td></tr></tbody></table>

В данном случае при изменении значении срабатывает функция change в которой измененяем текст метки label в соответствии с новым значением

![Обработка изменения значения в Spinbox в Tkinter и Python](https://metanit.com/python/tkinter/2.16.php./pics/2.72.png)

### Установка набора значений

Данный виджет необязательно должен представлять список из числовых значений. В реальности это может быть любой набор значений в виде списка или кортежа, который можно установить с помощью параметра values:

[?](https://metanit.com/python/tkinter/2.16.php#)

<table border="0" cellpadding="0" cellspacing="0"><tbody><tr><td class="gutter"><div class="line number1 index0 alt2">1</div><div class="line number2 index1 alt1">2</div><div class="line number3 index2 alt2">3</div><div class="line number4 index3 alt1">4</div><div class="line number5 index4 alt2">5</div><div class="line number6 index5 alt1">6</div><div class="line number7 index6 alt2">7</div><div class="line number8 index7 alt1">8</div><div class="line number9 index8 alt2">9</div><div class="line number10 index9 alt1">10</div><div class="line number11 index10 alt2">11</div><div class="line number12 index11 alt1">12</div><div class="line number13 index12 alt2">13</div><div class="line number14 index13 alt1">14</div><div class="line number15 index14 alt2">15</div><div class="line number16 index15 alt1">16</div><div class="line number17 index16 alt2">17</div><div class="line number18 index17 alt1">18</div></td><td class="code"><div class="container"><div class="line number1 index0 alt2"><code class="py keyword">from</code> <code class="py plain">tkinter </code><code class="py keyword">import</code> <code class="py keyword">*</code></div><div class="line number2 index1 alt1"><code class="py keyword">from</code> <code class="py plain">tkinter </code><code class="py keyword">import</code> <code class="py plain">ttk</code></div><div class="line number3 index2 alt2">&nbsp;</div><div class="line number4 index3 alt1"><code class="py plain">root </code><code class="py keyword">=</code> <code class="py plain">Tk()</code></div><div class="line number5 index4 alt2"><code class="py plain">root.title(</code><code class="py string">"METANIT.COM"</code><code class="py plain">)</code></div><div class="line number6 index5 alt1"><code class="py plain">root.geometry(</code><code class="py string">"250x150"</code><code class="py plain">)</code></div><div class="line number7 index6 alt2">&nbsp;</div><div class="line number8 index7 alt1"><code class="py plain">spinbox_var </code><code class="py keyword">=</code> <code class="py plain">StringVar()</code></div><div class="line number9 index8 alt2">&nbsp;</div><div class="line number10 index9 alt1"><code class="py plain">languages</code><code class="py keyword">=</code><code class="py plain">[</code><code class="py string">"Python"</code><code class="py plain">, </code><code class="py string">"JavaScript"</code><code class="py plain">, </code><code class="py string">"C#"</code><code class="py plain">, </code><code class="py string">"Java"</code><code class="py plain">, </code><code class="py string">"C++"</code><code class="py plain">]</code></div><div class="line number11 index10 alt2">&nbsp;</div><div class="line number12 index11 alt1"><code class="py plain">label </code><code class="py keyword">=</code> <code class="py plain">ttk.Label(textvariable</code><code class="py keyword">=</code><code class="py plain">spinbox_var)</code></div><div class="line number13 index12 alt2"><code class="py plain">label.pack(anchor</code><code class="py keyword">=</code><code class="py plain">NW)</code></div><div class="line number14 index13 alt1">&nbsp;</div><div class="line number15 index14 alt2"><code class="py plain">spinbox </code><code class="py keyword">=</code> <code class="py plain">ttk.Spinbox(textvariable</code><code class="py keyword">=</code><code class="py plain">spinbox_var, values</code><code class="py keyword">=</code><code class="py plain">languages)</code></div><div class="line number16 index15 alt1"><code class="py plain">spinbox.pack(anchor</code><code class="py keyword">=</code><code class="py plain">NW)</code></div><div class="line number17 index16 alt2">&nbsp;</div><div class="line number18 index17 alt1"><code class="py plain">root.mainloop()</code></div></div></td></tr></tbody></table>

В данном случае Spinbox позволяет выбрать одно из значений из списка languages:

![Установка значений в Spinbox в Tkinter и Python](https://metanit.com/python/tkinter/2.16.php./pics/2.75.png)