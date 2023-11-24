Виджет Notebook представляет набор вкладок. Среди параметров виджета следует выделить следующие:

-   width: ширина виджета
    
-   height: высота виджета
    
-   cursor: курсор при наведении на виджет
    
-   padding: отступы от границ виджета до его содержимого
    
-   style: стиль виджета
    

Для управления вкладками Notebook предоставляет ряд методов, в частности, для добавления вкладки применяется метод add()

[?](https://metanit.com/python/tkinter/2.19.php#)

<table border="0" cellpadding="0" cellspacing="0"><tbody><tr><td class="gutter"><div class="line number1 index0 alt2">1</div></td><td class="code"><div class="container"><div class="line number1 index0 alt2"><code class="py plain">add(child, state, sticky, padding, text, image, compound, underline)</code></div></div></td></tr></tbody></table>

Параметры метода

-   `child`: добавляемый виджет, для которого собственно и создается вкладка. Обычно это Frame, который затем добавляет другие виджеты
    
-   `state`: состояние вкладки. Возможные значения: "normal", "disabled", "hidden"
    
-   `sticky`: определяет прикрепление виджета к определенной стороне вкладки
    
-   `padding`: отступы от границ вкладки до внутреннего содержимого
    
-   `text`: заголовок вкладки
    
-   `image`: изображение в заголовке вкладке
    
-   `compound`: управляет расположением изображения и текста в заголовке вкладки
    
-   `underline`: определяет номер подчеркнутого символа в заголовке вкладки
    

Кроме того, чтобы скрыть временно вкладку, применяется метод hide()

[?](https://metanit.com/python/tkinter/2.19.php#)

<table border="0" cellpadding="0" cellspacing="0"><tbody><tr><td class="gutter"><div class="line number1 index0 alt2">1</div></td><td class="code"><div class="container"><div class="line number1 index0 alt2"><code class="py plain">hide(tabId)</code></div></div></td></tr></tbody></table>

В качестве параметра принимает идентификатор вкладки, который по умолчанию представляет числовой индекс вкладки начиная с 0.

Чтобы совсем удалить вкладку, применяется метод forget()

[?](https://metanit.com/python/tkinter/2.19.php#)

<table border="0" cellpadding="0" cellspacing="0"><tbody><tr><td class="gutter"><div class="line number1 index0 alt2">1</div></td><td class="code"><div class="container"><div class="line number1 index0 alt2"><code class="py plain">forget(child)</code></div></div></td></tr></tbody></table>

В качестве параметра в метод передается удаляемый виджет.

Рассмотрим простейший пример:

[?](https://metanit.com/python/tkinter/2.19.php#)

<table border="0" cellpadding="0" cellspacing="0"><tbody><tr><td class="gutter"><div class="line number1 index0 alt2">1</div><div class="line number2 index1 alt1">2</div><div class="line number3 index2 alt2">3</div><div class="line number4 index3 alt1">4</div><div class="line number5 index4 alt2">5</div><div class="line number6 index5 alt1">6</div><div class="line number7 index6 alt2">7</div><div class="line number8 index7 alt1">8</div><div class="line number9 index8 alt2">9</div><div class="line number10 index9 alt1">10</div><div class="line number11 index10 alt2">11</div><div class="line number12 index11 alt1">12</div><div class="line number13 index12 alt2">13</div><div class="line number14 index13 alt1">14</div><div class="line number15 index14 alt2">15</div><div class="line number16 index15 alt1">16</div><div class="line number17 index16 alt2">17</div><div class="line number18 index17 alt1">18</div><div class="line number19 index18 alt2">19</div><div class="line number20 index19 alt1">20</div><div class="line number21 index20 alt2">21</div><div class="line number22 index21 alt1">22</div><div class="line number23 index22 alt2">23</div></td><td class="code"><div class="container"><div class="line number1 index0 alt2"><code class="py keyword">from</code> <code class="py plain">tkinter </code><code class="py keyword">import</code> <code class="py keyword">*</code></div><div class="line number2 index1 alt1"><code class="py keyword">from</code> <code class="py plain">tkinter </code><code class="py keyword">import</code> <code class="py plain">ttk</code></div><div class="line number3 index2 alt2">&nbsp;</div><div class="line number4 index3 alt1"><code class="py plain">root </code><code class="py keyword">=</code> <code class="py plain">Tk()</code></div><div class="line number5 index4 alt2"><code class="py plain">root.title(</code><code class="py string">"METANIT.COM"</code><code class="py plain">)</code></div><div class="line number6 index5 alt1"><code class="py plain">root.geometry(</code><code class="py string">"250x200"</code><code class="py plain">)</code></div><div class="line number7 index6 alt2">&nbsp;</div><div class="line number8 index7 alt1"><code class="py comments"># создаем набор вкладок</code></div><div class="line number9 index8 alt2"><code class="py plain">notebook </code><code class="py keyword">=</code> <code class="py plain">ttk.Notebook()</code></div><div class="line number10 index9 alt1"><code class="py plain">notebook.pack(expand</code><code class="py keyword">=</code><code class="py color1">True</code><code class="py plain">, fill</code><code class="py keyword">=</code><code class="py plain">BOTH)</code></div><div class="line number11 index10 alt2">&nbsp;</div><div class="line number12 index11 alt1"><code class="py comments"># создаем пару фреймвов</code></div><div class="line number13 index12 alt2"><code class="py plain">frame1 </code><code class="py keyword">=</code> <code class="py plain">ttk.Frame(notebook)</code></div><div class="line number14 index13 alt1"><code class="py plain">frame2 </code><code class="py keyword">=</code> <code class="py plain">ttk.Frame(notebook)</code></div><div class="line number15 index14 alt2">&nbsp;</div><div class="line number16 index15 alt1"><code class="py plain">frame1.pack(fill</code><code class="py keyword">=</code><code class="py plain">BOTH, expand</code><code class="py keyword">=</code><code class="py color1">True</code><code class="py plain">)</code></div><div class="line number17 index16 alt2"><code class="py plain">frame2.pack(fill</code><code class="py keyword">=</code><code class="py plain">BOTH, expand</code><code class="py keyword">=</code><code class="py color1">True</code><code class="py plain">)</code></div><div class="line number18 index17 alt1">&nbsp;</div><div class="line number19 index18 alt2"><code class="py comments"># добавляем фреймы в качестве вкладок</code></div><div class="line number20 index19 alt1"><code class="py plain">notebook.add(frame1, text</code><code class="py keyword">=</code><code class="py string">"Python"</code><code class="py plain">)</code></div><div class="line number21 index20 alt2"><code class="py plain">notebook.add(frame2, text</code><code class="py keyword">=</code><code class="py string">"Java"</code><code class="py plain">)</code></div><div class="line number22 index21 alt1">&nbsp;</div><div class="line number23 index22 alt2"><code class="py plain">root.mainloop()</code></div></div></td></tr></tbody></table>

Здесь определяются два фрейма, для которых создаются отдельные вкладки

![Notebook и создание вкладок в Tkinter и Python](https://metanit.com/python/tkinter/2.19.php./pics/2.85.png)

### Добавление изображений

За установку изображения в заголовке вкладки отвечает параметр image метода add. Кроме того, с помощью параметра compound можно задать расположение картинки относительно текста. В частности, параметр compound может принимать следующие значения:

-   top: изображение поверх текста
    
-   bottom: изображение под текстом
    
-   left: изображение слева от текста
    
-   right: изображение справа от текста
    
-   none: при наличии изображения отображается только изображение
    
-   text: отображается только текст
    
-   image: отображается только изображение
    

Например, отобразим картинку слева от текста:

[?](https://metanit.com/python/tkinter/2.19.php#)

<table border="0" cellpadding="0" cellspacing="0"><tbody><tr><td class="gutter"><div class="line number1 index0 alt2">1</div><div class="line number2 index1 alt1">2</div><div class="line number3 index2 alt2">3</div><div class="line number4 index3 alt1">4</div><div class="line number5 index4 alt2">5</div><div class="line number6 index5 alt1">6</div><div class="line number7 index6 alt2">7</div><div class="line number8 index7 alt1">8</div><div class="line number9 index8 alt2">9</div><div class="line number10 index9 alt1">10</div><div class="line number11 index10 alt2">11</div><div class="line number12 index11 alt1">12</div><div class="line number13 index12 alt2">13</div><div class="line number14 index13 alt1">14</div><div class="line number15 index14 alt2">15</div><div class="line number16 index15 alt1">16</div><div class="line number17 index16 alt2">17</div><div class="line number18 index17 alt1">18</div><div class="line number19 index18 alt2">19</div><div class="line number20 index19 alt1">20</div><div class="line number21 index20 alt2">21</div><div class="line number22 index21 alt1">22</div><div class="line number23 index22 alt2">23</div><div class="line number24 index23 alt1">24</div><div class="line number25 index24 alt2">25</div></td><td class="code"><div class="container"><div class="line number1 index0 alt2"><code class="py keyword">from</code> <code class="py plain">tkinter </code><code class="py keyword">import</code> <code class="py keyword">*</code></div><div class="line number2 index1 alt1"><code class="py keyword">from</code> <code class="py plain">tkinter </code><code class="py keyword">import</code> <code class="py plain">ttk</code></div><div class="line number3 index2 alt2">&nbsp;</div><div class="line number4 index3 alt1"><code class="py plain">root </code><code class="py keyword">=</code> <code class="py plain">Tk()</code></div><div class="line number5 index4 alt2"><code class="py plain">root.title(</code><code class="py string">"METANIT.COM"</code><code class="py plain">)</code></div><div class="line number6 index5 alt1"><code class="py plain">root.geometry(</code><code class="py string">"250x200"</code><code class="py plain">)</code></div><div class="line number7 index6 alt2">&nbsp;</div><div class="line number8 index7 alt1"><code class="py comments"># создаем набор вкладок</code></div><div class="line number9 index8 alt2"><code class="py plain">notebook </code><code class="py keyword">=</code> <code class="py plain">ttk.Notebook()</code></div><div class="line number10 index9 alt1"><code class="py plain">notebook.pack(expand</code><code class="py keyword">=</code><code class="py color1">True</code><code class="py plain">, fill</code><code class="py keyword">=</code><code class="py plain">BOTH)</code></div><div class="line number11 index10 alt2">&nbsp;</div><div class="line number12 index11 alt1"><code class="py comments"># создаем пару фреймвов</code></div><div class="line number13 index12 alt2"><code class="py plain">frame1 </code><code class="py keyword">=</code> <code class="py plain">ttk.Frame(notebook)</code></div><div class="line number14 index13 alt1"><code class="py plain">frame2 </code><code class="py keyword">=</code> <code class="py plain">ttk.Frame(notebook)</code></div><div class="line number15 index14 alt2">&nbsp;</div><div class="line number16 index15 alt1"><code class="py plain">frame1.pack(fill</code><code class="py keyword">=</code><code class="py plain">BOTH, expand</code><code class="py keyword">=</code><code class="py color1">True</code><code class="py plain">)</code></div><div class="line number17 index16 alt2"><code class="py plain">frame2.pack(fill</code><code class="py keyword">=</code><code class="py plain">BOTH, expand</code><code class="py keyword">=</code><code class="py color1">True</code><code class="py plain">)</code></div><div class="line number18 index17 alt1">&nbsp;</div><div class="line number19 index18 alt2"><code class="py plain">python_logo </code><code class="py keyword">=</code> <code class="py plain">PhotoImage(</code><code class="py functions">file</code><code class="py keyword">=</code><code class="py string">"./python_mc.png"</code><code class="py plain">)</code></div><div class="line number20 index19 alt1"><code class="py plain">java_logo </code><code class="py keyword">=</code> <code class="py plain">PhotoImage(</code><code class="py functions">file</code><code class="py keyword">=</code><code class="py string">"./java_mc.png"</code><code class="py plain">)</code></div><div class="line number21 index20 alt2"><code class="py comments"># добавляем фреймы в качестве вкладок</code></div><div class="line number22 index21 alt1"><code class="py plain">notebook.add(frame1, text</code><code class="py keyword">=</code><code class="py string">"Python"</code><code class="py plain">, image</code><code class="py keyword">=</code><code class="py plain">python_logo, compound</code><code class="py keyword">=</code><code class="py plain">LEFT)</code></div><div class="line number23 index22 alt2"><code class="py plain">notebook.add(frame2, text</code><code class="py keyword">=</code><code class="py string">"Java"</code><code class="py plain">, image</code><code class="py keyword">=</code><code class="py plain">java_logo, compound</code><code class="py keyword">=</code><code class="py plain">LEFT)</code></div><div class="line number24 index23 alt1">&nbsp;</div><div class="line number25 index24 alt2"><code class="py plain">root.mainloop()</code></div></div></td></tr></tbody></table>

Следует отметить, что высота заголовка вкладки устанавливается в соответствии с высотой картинки: