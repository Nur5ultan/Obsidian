Многие программы на сегодняшний день используют графический интерфейс, который более интуитивен и удобен для пользователя, чем консоль. И с помощью языка программирования Python также можно создавать графические программы. Для этого в Python по умолчанию применяется специальный тулкит - набор компонентов, который называется tkinter. Тулкит tkinter доступен в виде отдельного встроенного модуля, который содержит все необходимые графические компоненты - кнопки, текстовые поля и т.д.

По сути Tkinter представляет интерфейс в Python для графической библиотеки Tk (Собственно само название "Tkinter" является сокращением "Tk interface"). Первоначально данная библиотека разрабатывалась для языка Tcl - ее создал в 1988 году Джон Остерхаут (John Ousterhout), профессор computer science из Беркли для создания графических приложений для своего языка Tcl. Но впоследствии Tk была адаптирована для широкого ряда динамических языков, в частности, для Ruby, Perl и естественно для языка Python (в 1994 году). И на сегодняшний день и библиотека Tk, и сам тулкит tkinter доступны для большинства операционных систем, в том числе для Mac OS, Linux и Windows.

Преимущества Tkinter:

-   Данный тулкит по умолчанию включен в стандартную библиотеку языка Python в виде отдельного модуля, поэтому не потребуется что-то дополнительно устанавливать
    
-   Tkinter - кроссплатформенный, один и тот же код будет работать одинаково на разных платформах (Mac OS, Linux и Windows)
    
-   Tkinter легко изучать. Сам тулкит, хотя и содержит некоторый готовый код, виджеты и графические элементы, но при этом довольно лаконичен и прост.
    
-   Tk распространяется по BSD-лицензии, поэтому библиотека может быть использована как в опенсорсных проектах, так и в коммерческих наработках.
    

Если необходимо или интересно узнать версию библиотеки Tk, которая будет использоваться, в интерпертаторе Python можно выполнить следующую инструкцию:

[?](https://metanit.com/python/tkinter/1.1.php#)

<table border="0" cellpadding="0" cellspacing="0"><tbody><tr><td class="gutter"><div class="line number1 index0 alt2">1</div></td><td class="code"><div class="container"><div class="line number1 index0 alt2"><code class="py plain">tkinter.Tcl().</code><code class="py functions">eval</code><code class="py plain">(</code><code class="py string">"info patchlevel"</code><code class="py plain">)</code></div></div></td></tr></tbody></table>

```
C:\Users\eugen>python
Python 3.10.1 (tags/v3.10.1:2cd268a, Dec  6 2021, 19:10:37) [MSC v.1929 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>> import tkinter
>>>
>>> tkinter.Tcl().eval("info patchlevel")
'8.6.12'
>>>

```

В некоторых ОС на базе Linux иногда при установке python не устанавливается пакет tkinter. В этом случае мы можем доустановить thinkter командой

```
 sudo apt-get install python3-tk
```

### Первая программа

Создадим первую программу с использованием Tkinter. Для этого определим следующий скрипт:

[?](https://metanit.com/python/tkinter/1.1.php#)

<table border="0" cellpadding="0" cellspacing="0"><tbody><tr><td class="gutter"><div class="line number1 index0 alt2">1</div><div class="line number2 index1 alt1">2</div><div class="line number3 index2 alt2">3</div><div class="line number4 index3 alt1">4</div><div class="line number5 index4 alt2">5</div><div class="line number6 index5 alt1">6</div><div class="line number7 index6 alt2">7</div><div class="line number8 index7 alt1">8</div><div class="line number9 index8 alt2">9</div><div class="line number10 index9 alt1">10</div></td><td class="code"><div class="container"><div class="line number1 index0 alt2"><code class="py keyword">from</code> <code class="py plain">tkinter </code><code class="py keyword">import</code> <code class="py keyword">*</code></div><div class="line number2 index1 alt1">&nbsp;</div><div class="line number3 index2 alt2"><code class="py plain">root </code><code class="py keyword">=</code> <code class="py plain">Tk()&nbsp;&nbsp;&nbsp;&nbsp; </code><code class="py comments"># создаем корневой объект - окно</code></div><div class="line number4 index3 alt1"><code class="py plain">root.title(</code><code class="py string">"Приложение на Tkinter"</code><code class="py plain">)&nbsp;&nbsp;&nbsp;&nbsp; </code><code class="py comments"># устанавливаем заголовок окна</code></div><div class="line number5 index4 alt2"><code class="py plain">root.geometry(</code><code class="py string">"300x250"</code><code class="py plain">)&nbsp;&nbsp;&nbsp; </code><code class="py comments"># устанавливаем размеры окна</code></div><div class="line number6 index5 alt1">&nbsp;</div><div class="line number7 index6 alt2"><code class="py plain">label </code><code class="py keyword">=</code> <code class="py plain">Label(text</code><code class="py keyword">=</code><code class="py string">"Hello METANIT.COM"</code><code class="py plain">) </code><code class="py comments"># создаем текстовую метку</code></div><div class="line number8 index7 alt1"><code class="py plain">label.pack()&nbsp;&nbsp;&nbsp; </code><code class="py comments"># размещаем метку в окне</code></div><div class="line number9 index8 alt2">&nbsp;</div><div class="line number10 index9 alt1"><code class="py plain">root.mainloop()</code></div></div></td></tr></tbody></table>

Для создания графического окна применяется конструктор Tk(), который определен в модуле tkinter. Создаваемое окно присваивается переменной root, и через эту переменную мы можем управлять атрибутами окна. В частности, с помощью метода title() можно установить заголовок окна.

С помощью метода geometry() - размер окна. Для установки размера в метод `geometry()` передается строка в формате "Ширина x Высота". Если при создании окна приложения метод `geometry()` не вызывается, то окно занимает то пространство, которое необходимо для размещения внутреннего содержимого.

Создав окно, мы можем разместить в нем другие графические элементы. Эти элементы еще называются виджетами. В данном случае мы размещаем в окне текстовую метку. Для это создаем объект класса Label, которые хранит некоторый текст. Затем для размещения элемента label в окне вызываем у него метод `pack()`

Для отображения окна надо вызвать у него метод mainloop(), который запускает цикл обработки событий окна для взаимодействия с пользователем.

В результате при запуске скрипта мы увидим такое пустое окошко:

![[Files/Pasted image 20231024002902.png]]

На скриншоте выше определено окно, создаваемое в ОС Windows, на каждой конкретной системе отдельные визуальные моменты, отрисовка графических компонентов может несколько отличаться.