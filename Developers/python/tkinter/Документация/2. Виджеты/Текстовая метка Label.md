Виджет Label представляет текстовую метку. Этот элемент позволяет выводить статический текст без возможности редактирования.

Для создания элемента Label применяется конструктор, который принимает два параметра:

[?](https://metanit.com/python/tkinter/2.7.php#)

<table border="0" cellpadding="0" cellspacing="0"><tbody><tr><td class="gutter"><div class="line number1 index0 alt2">1</div></td><td class="code"><div class="container"><div class="line number1 index0 alt2"><code class="py plain">Label(master, options)</code></div></div></td></tr></tbody></table>

Параметр master представляет ссылку на родительский контейнер, а параметр options представляет следующие именованные параметры

-   anchor: устанавливает позиционирование текста
    
-   background: фоновый цвет
    
-   borderwidth: толщина границы метки
    
-   cursor: курсор указателя мыши при наведении на метку
    
-   font: шрифт текста
    
-   foreground: цвет текста
    
-   height: высота виджета
    
-   image: ссылка на изображение, которое отображается на метке
    
-   justify: устанавливает выравнивание текста. Значение LEFT выравнивает текст по левому краю, CENTER - по центру, RIGHT - по правому краю
    
-   pading: отступы от границ вилжета до его текста
    
-   relief: определяет тип границы, по умолчанию значение FLAT
    
-   text: устанавливает текст метки
    
-   textvariable: устанавливает привязку к элементу StringVar
    
-   underline: указывает на номер символа в тексте метки, который подчеркивается. По умолчанию значение -1, то есть никакой символ не подчеркивается
    
-   width: ширина виджета
    
-   wraplength: при положительном значении строки текста будут переносится для вмещения в пространство виджета
    

Выведем в окне приложения простейший текст:

[?](https://metanit.com/python/tkinter/2.7.php#)

<table border="0" cellpadding="0" cellspacing="0"><tbody><tr><td class="gutter"><div class="line number1 index0 alt2">1</div><div class="line number2 index1 alt1">2</div><div class="line number3 index2 alt2">3</div><div class="line number4 index3 alt1">4</div><div class="line number5 index4 alt2">5</div><div class="line number6 index5 alt1">6</div><div class="line number7 index6 alt2">7</div><div class="line number8 index7 alt1">8</div><div class="line number9 index8 alt2">9</div><div class="line number10 index9 alt1">10</div><div class="line number11 index10 alt2">11</div></td><td class="code"><div class="container"><div class="line number1 index0 alt2"><code class="py keyword">from</code> <code class="py plain">tkinter </code><code class="py keyword">import</code> <code class="py keyword">*</code></div><div class="line number2 index1 alt1"><code class="py keyword">from</code> <code class="py plain">tkinter </code><code class="py keyword">import</code> <code class="py plain">ttk</code></div><div class="line number3 index2 alt2">&nbsp;</div><div class="line number4 index3 alt1"><code class="py plain">root </code><code class="py keyword">=</code> <code class="py plain">Tk()</code></div><div class="line number5 index4 alt2"><code class="py plain">root.title(</code><code class="py string">"METANIT.COM"</code><code class="py plain">)</code></div><div class="line number6 index5 alt1"><code class="py plain">root.geometry(</code><code class="py string">"250x200"</code><code class="py plain">)</code></div><div class="line number7 index6 alt2">&nbsp;</div><div class="line number8 index7 alt1"><code class="py plain">label </code><code class="py keyword">=</code> <code class="py plain">ttk.Label(text</code><code class="py keyword">=</code><code class="py string">"Hello METANIT.COM"</code><code class="py plain">)</code></div><div class="line number9 index8 alt2"><code class="py plain">label.pack()</code></div><div class="line number10 index9 alt1">&nbsp;</div><div class="line number11 index10 alt2"><code class="py plain">root.mainloop()</code></div></div></td></tr></tbody></table>

![Label в tkinter и Python](https://metanit.com/python/tkinter/2.7.php./pics/2.28.png)

### Установка шрифта

Параметр font принимает определение шрифта в виде:

[?](https://metanit.com/python/tkinter/2.7.php#)

<table border="0" cellpadding="0" cellspacing="0"><tbody><tr><td class="gutter"><div class="line number1 index0 alt2">1</div></td><td class="code"><div class="container"><div class="line number1 index0 alt2"><code class="py plain">font </code><code class="py keyword">=</code> <code class="py plain">(</code><code class="py string">"имя шрифта"</code><code class="py plain">, размер_шрифта)</code></div></div></td></tr></tbody></table>

Первое значение передает имя шрифта в кавычках, а второе - числовой размер шрифта. Например, установим шрифт Arial высотой в 14 единиц:

[?](https://metanit.com/python/tkinter/2.7.php#)

<table border="0" cellpadding="0" cellspacing="0"><tbody><tr><td class="gutter"><div class="line number1 index0 alt2">1</div><div class="line number2 index1 alt1">2</div><div class="line number3 index2 alt2">3</div><div class="line number4 index3 alt1">4</div><div class="line number5 index4 alt2">5</div><div class="line number6 index5 alt1">6</div><div class="line number7 index6 alt2">7</div><div class="line number8 index7 alt1">8</div><div class="line number9 index8 alt2">9</div><div class="line number10 index9 alt1">10</div><div class="line number11 index10 alt2">11</div></td><td class="code"><div class="container"><div class="line number1 index0 alt2"><code class="py keyword">from</code> <code class="py plain">tkinter </code><code class="py keyword">import</code> <code class="py keyword">*</code></div><div class="line number2 index1 alt1"><code class="py keyword">from</code> <code class="py plain">tkinter </code><code class="py keyword">import</code> <code class="py plain">ttk</code></div><div class="line number3 index2 alt2">&nbsp;</div><div class="line number4 index3 alt1"><code class="py plain">root </code><code class="py keyword">=</code> <code class="py plain">Tk()</code></div><div class="line number5 index4 alt2"><code class="py plain">root.title(</code><code class="py string">"METANIT.COM"</code><code class="py plain">)</code></div><div class="line number6 index5 alt1"><code class="py plain">root.geometry(</code><code class="py string">"250x200"</code><code class="py plain">)</code></div><div class="line number7 index6 alt2">&nbsp;</div><div class="line number8 index7 alt1"><code class="py plain">label </code><code class="py keyword">=</code> <code class="py plain">ttk.Label(text</code><code class="py keyword">=</code><code class="py string">"Hello METANIT.COM"</code><code class="py plain">, font</code><code class="py keyword">=</code><code class="py plain">(</code><code class="py string">"Arial"</code><code class="py plain">, </code><code class="py value">14</code><code class="py plain">))</code></div><div class="line number9 index8 alt2"><code class="py plain">label.pack()</code></div><div class="line number10 index9 alt1">&nbsp;</div><div class="line number11 index10 alt2"><code class="py plain">root.mainloop()</code></div></div></td></tr></tbody></table>

![Шрифт текста в Label в tkinter и Python](https://metanit.com/python/tkinter/2.7.php./pics/2.29.png)

### Установка изображения

За установку изображения на метке отвечает параметр image. Самый простой способ определения изображения представляет создание объекта PhotoImage, в конструктор которого передается путь к изображению:

[?](https://metanit.com/python/tkinter/2.7.php#)

<table border="0" cellpadding="0" cellspacing="0"><tbody><tr><td class="gutter"><div class="line number1 index0 alt2">1</div><div class="line number2 index1 alt1">2</div><div class="line number3 index2 alt2">3</div><div class="line number4 index3 alt1">4</div><div class="line number5 index4 alt2">5</div><div class="line number6 index5 alt1">6</div><div class="line number7 index6 alt2">7</div><div class="line number8 index7 alt1">8</div><div class="line number9 index8 alt2">9</div><div class="line number10 index9 alt1">10</div><div class="line number11 index10 alt2">11</div><div class="line number12 index11 alt1">12</div><div class="line number13 index12 alt2">13</div></td><td class="code"><div class="container"><div class="line number1 index0 alt2"><code class="py keyword">from</code> <code class="py plain">tkinter </code><code class="py keyword">import</code> <code class="py keyword">*</code></div><div class="line number2 index1 alt1"><code class="py keyword">from</code> <code class="py plain">tkinter </code><code class="py keyword">import</code> <code class="py plain">ttk</code></div><div class="line number3 index2 alt2">&nbsp;</div><div class="line number4 index3 alt1"><code class="py plain">root </code><code class="py keyword">=</code> <code class="py plain">Tk()</code></div><div class="line number5 index4 alt2"><code class="py plain">root.title(</code><code class="py string">"METANIT.COM"</code><code class="py plain">)</code></div><div class="line number6 index5 alt1"><code class="py plain">root.geometry(</code><code class="py string">"250x200"</code><code class="py plain">)</code></div><div class="line number7 index6 alt2">&nbsp;</div><div class="line number8 index7 alt1"><code class="py plain">python_logo </code><code class="py keyword">=</code> <code class="py plain">PhotoImage(</code><code class="py functions">file</code><code class="py keyword">=</code><code class="py string">"./python_logo.png"</code><code class="py plain">)</code></div><div class="line number9 index8 alt2">&nbsp;</div><div class="line number10 index9 alt1"><code class="py plain">label </code><code class="py keyword">=</code> <code class="py plain">ttk.Label(image</code><code class="py keyword">=</code><code class="py plain">python_logo)</code></div><div class="line number11 index10 alt2"><code class="py plain">label.pack()</code></div><div class="line number12 index11 alt1">&nbsp;</div><div class="line number13 index12 alt2"><code class="py plain">root.mainloop()</code></div></div></td></tr></tbody></table>

В моем случае изображение представляет файл python\_logo.png, которое находится в одной папке с файлом приложения и которое изображает логотип python:

![изображение в Label в tkinter и Python](https://metanit.com/python/tkinter/2.7.php./pics/2.30.png)

Если необходимо также отображать и текст, то для этого можно установить параметр compound, который определяет положение текста по отношению к изображению с помощью одного из следующих значений:

-   top: изображение поверх текста
    
-   bottom: изображение под текстом
    
-   left: изображение слева от текста
    
-   right: изображение справа от текста
    
-   none: при наличии изображения отображается только изображение
    
-   text: отображается только текст
    
-   image: отображается только изображение
    

Например, отобразим картинку поверх текста:

[?](https://metanit.com/python/tkinter/2.7.php#)

<table border="0" cellpadding="0" cellspacing="0"><tbody><tr><td class="gutter"><div class="line number1 index0 alt2">1</div><div class="line number2 index1 alt1">2</div><div class="line number3 index2 alt2">3</div><div class="line number4 index3 alt1">4</div><div class="line number5 index4 alt2">5</div><div class="line number6 index5 alt1">6</div><div class="line number7 index6 alt2">7</div><div class="line number8 index7 alt1">8</div><div class="line number9 index8 alt2">9</div><div class="line number10 index9 alt1">10</div><div class="line number11 index10 alt2">11</div><div class="line number12 index11 alt1">12</div><div class="line number13 index12 alt2">13</div></td><td class="code"><div class="container"><div class="line number1 index0 alt2"><code class="py keyword">from</code> <code class="py plain">tkinter </code><code class="py keyword">import</code> <code class="py keyword">*</code></div><div class="line number2 index1 alt1"><code class="py keyword">from</code> <code class="py plain">tkinter </code><code class="py keyword">import</code> <code class="py plain">ttk</code></div><div class="line number3 index2 alt2">&nbsp;</div><div class="line number4 index3 alt1"><code class="py plain">root </code><code class="py keyword">=</code> <code class="py plain">Tk()</code></div><div class="line number5 index4 alt2"><code class="py plain">root.title(</code><code class="py string">"METANIT.COM"</code><code class="py plain">)</code></div><div class="line number6 index5 alt1"><code class="py plain">root.geometry(</code><code class="py string">"250x200"</code><code class="py plain">)</code></div><div class="line number7 index6 alt2">&nbsp;</div><div class="line number8 index7 alt1"><code class="py plain">python_logo </code><code class="py keyword">=</code> <code class="py plain">PhotoImage(</code><code class="py functions">file</code><code class="py keyword">=</code><code class="py string">"./python_logo.png"</code><code class="py plain">)</code></div><div class="line number9 index8 alt2">&nbsp;</div><div class="line number10 index9 alt1"><code class="py plain">label </code><code class="py keyword">=</code> <code class="py plain">ttk.Label(image</code><code class="py keyword">=</code><code class="py plain">python_logo, text</code><code class="py keyword">=</code><code class="py string">"Python"</code><code class="py plain">, compound</code><code class="py keyword">=</code><code class="py string">"top"</code><code class="py plain">)</code></div><div class="line number11 index10 alt2"><code class="py plain">label.pack()</code></div><div class="line number12 index11 alt1">&nbsp;</div><div class="line number13 index12 alt2"><code class="py plain">root.mainloop()</code></div></div></td></tr></tbody></table>

![Картинка с текстов в label в tkinter в Python](https://metanit.com/python/tkinter/2.7.php./pics/2.31.png)

### Стилизация

По умолчанию метка не имеет границы. Для установки толщины границы используется параметр borderwidth, при этом нам также надо установить тип границы с помощью параметра releaf, который может принимать значения: "flat", "raised", "sunken", "ridge", "solid" и "groove":

[?](https://metanit.com/python/tkinter/2.7.php#)

<table border="0" cellpadding="0" cellspacing="0"><tbody><tr><td class="gutter"><div class="line number1 index0 alt2">1</div><div class="line number2 index1 alt1">2</div><div class="line number3 index2 alt2">3</div><div class="line number4 index3 alt1">4</div><div class="line number5 index4 alt2">5</div><div class="line number6 index5 alt1">6</div><div class="line number7 index6 alt2">7</div><div class="line number8 index7 alt1">8</div><div class="line number9 index8 alt2">9</div><div class="line number10 index9 alt1">10</div><div class="line number11 index10 alt2">11</div><div class="line number12 index11 alt1">12</div></td><td class="code"><div class="container"><div class="line number1 index0 alt2"><code class="py keyword">from</code> <code class="py plain">tkinter </code><code class="py keyword">import</code> <code class="py keyword">*</code></div><div class="line number2 index1 alt1"><code class="py keyword">from</code> <code class="py plain">tkinter </code><code class="py keyword">import</code> <code class="py plain">ttk</code></div><div class="line number3 index2 alt2">&nbsp;</div><div class="line number4 index3 alt1"><code class="py plain">root </code><code class="py keyword">=</code> <code class="py plain">Tk()</code></div><div class="line number5 index4 alt2"><code class="py plain">root.title(</code><code class="py string">"METANIT.COM"</code><code class="py plain">)</code></div><div class="line number6 index5 alt1"><code class="py plain">root.geometry(</code><code class="py string">"250x200"</code><code class="py plain">)</code></div><div class="line number7 index6 alt2">&nbsp;</div><div class="line number8 index7 alt1">&nbsp;</div><div class="line number9 index8 alt2"><code class="py plain">label </code><code class="py keyword">=</code> <code class="py plain">ttk.Label(text</code><code class="py keyword">=</code><code class="py string">"Hello Tkinter"</code><code class="py plain">, borderwidth</code><code class="py keyword">=</code><code class="py value">2</code><code class="py plain">, relief</code><code class="py keyword">=</code><code class="py string">"ridge"</code><code class="py plain">, padding</code><code class="py keyword">=</code><code class="py value">8</code><code class="py plain">)</code></div><div class="line number10 index9 alt1"><code class="py plain">label.pack(expand</code><code class="py keyword">=</code><code class="py color1">True</code><code class="py plain">)</code></div><div class="line number11 index10 alt2">&nbsp;</div><div class="line number12 index11 alt1"><code class="py plain">root.mainloop()</code></div></div></td></tr></tbody></table>

Установка цвета фона и текста:

[?](https://metanit.com/python/tkinter/2.7.php#)

<table border="0" cellpadding="0" cellspacing="0"><tbody><tr><td class="gutter"><div class="line number1 index0 alt2">1</div><div class="line number2 index1 alt1">2</div><div class="line number3 index2 alt2">3</div><div class="line number4 index3 alt1">4</div><div class="line number5 index4 alt2">5</div><div class="line number6 index5 alt1">6</div><div class="line number7 index6 alt2">7</div><div class="line number8 index7 alt1">8</div><div class="line number9 index8 alt2">9</div><div class="line number10 index9 alt1">10</div><div class="line number11 index10 alt2">11</div><div class="line number12 index11 alt1">12</div></td><td class="code"><div class="container"><div class="line number1 index0 alt2"><code class="py keyword">from</code> <code class="py plain">tkinter </code><code class="py keyword">import</code> <code class="py keyword">*</code></div><div class="line number2 index1 alt1"><code class="py keyword">from</code> <code class="py plain">tkinter </code><code class="py keyword">import</code> <code class="py plain">ttk</code></div><div class="line number3 index2 alt2">&nbsp;</div><div class="line number4 index3 alt1"><code class="py plain">root </code><code class="py keyword">=</code> <code class="py plain">Tk()</code></div><div class="line number5 index4 alt2"><code class="py plain">root.title(</code><code class="py string">"METANIT.COM"</code><code class="py plain">)</code></div><div class="line number6 index5 alt1"><code class="py plain">root.geometry(</code><code class="py string">"250x200"</code><code class="py plain">)</code></div><div class="line number7 index6 alt2">&nbsp;</div><div class="line number8 index7 alt1">&nbsp;</div><div class="line number9 index8 alt2"><code class="py plain">label </code><code class="py keyword">=</code> <code class="py plain">ttk.Label(text</code><code class="py keyword">=</code><code class="py string">"Hello Tkinter"</code><code class="py plain">, background</code><code class="py keyword">=</code><code class="py string">"#FFCDD2"</code><code class="py plain">, foreground</code><code class="py keyword">=</code><code class="py string">"#B71C1C"</code><code class="py plain">, padding</code><code class="py keyword">=</code><code class="py value">8</code><code class="py plain">)</code></div><div class="line number10 index9 alt1"><code class="py plain">label.pack(expand</code><code class="py keyword">=</code><code class="py color1">True</code><code class="py plain">)</code></div><div class="line number11 index10 alt2">&nbsp;</div><div class="line number12 index11 alt1"><code class="py plain">root.mainloop()</code></div></div></td></tr></tbody></table>

![стилизация label в tkinter и python](https://metanit.com/python/tkinter/2.7.php./pics/2.32.png)