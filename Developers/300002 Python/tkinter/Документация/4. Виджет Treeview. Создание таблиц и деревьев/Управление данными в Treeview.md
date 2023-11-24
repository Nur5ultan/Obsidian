Виджет Treeview предназначен для отображения иерархических данных, причем как в виде дерева, так и в виде таблицы. Среди параметров Treeview следует отметить следующие:

-   columns: столбцы таблицы в виде строки или списка/кортежа строк
    
-   displaycolumns: отображаемые столбцы таблицы
    
-   cursor: курсор при наведении на виджет
    
-   height: высота виджета
    
-   padding: отступы от границ виджета до содержимого
    
-   selectmode: режим выбора элементов в виджете
    
-   show: формат отображения данных. Может принимать одно из следующих значений:
    
    -   `tree`: отображает столбец #0
        
    -   `heading`: отображает строку с заголовками
        
    -   `tree headings`: отображает столбец #0 и строку с заголовками
        
    -   `""`: не отображает ни столбец #0, ни строку с заголовками
        

### Управление данными

#### Добавление элементов

Для добавления данных применяется метод insert():

[?](https://metanit.com/python/tkinter/4.1.php#)

<table border="0" cellpadding="0" cellspacing="0"><tbody><tr><td class="gutter"><div class="line number1 index0 alt2">1</div></td><td class="code"><div class="container"><div class="line number1 index0 alt2"><code class="py plain">insert: (parent, index, iid, values) </code><code class="py keyword">-</code><code class="py plain">&gt; </code><code class="py functions">str</code></div></div></td></tr></tbody></table>

Этот метод создает новый элемент и возвращает его идентификатор, который по умолчанию представляет строку наподобие "IOO1". Основные параметры метода:

-   parent: представляет идентификатор родительского элемента, в который добавляется элемент. Если создается элемент верхнего уровня, для которого не существует никакого родительского элемента, как, например, в случае с добавлением строки в таблицу, то передается пустая строка.
    
-   index: указывает индекс для вставки элемента. Если элемент добавляется в конец, то используется значение `END` или `"end"`, либо указывается число, которое равно количеству элементов или больше его. Если элемент добавляется в самое начало, то указывается 0 или число меньше нуля.
    
-   iid: если указан данный параметр, то его значение будет использоваться в качестве идентификатора элемента. При этом подобный в виджете не должно быть элемента с подобным идентификатором, иначе генерируется новый идентификатор, как в обшем случае
    
-   values: список или кортеж значений, которые и составляют добавляемый элемент
    

#### Удаление элементов

Для удаления данных применяется метод delete():

[?](https://metanit.com/python/tkinter/4.1.php#)

<table border="0" cellpadding="0" cellspacing="0"><tbody><tr><td class="gutter"><div class="line number1 index0 alt2">1</div></td><td class="code"><div class="container"><div class="line number1 index0 alt2"><code class="py plain">delete(items)</code></div></div></td></tr></tbody></table>

В качестве параметра метод принимает удаляемые данные

#### Перемещение элементов

Для перемещения элемента на другую позицию применяется метод move():

[?](https://metanit.com/python/tkinter/4.1.php#)

<table border="0" cellpadding="0" cellspacing="0"><tbody><tr><td class="gutter"><div class="line number1 index0 alt2">1</div></td><td class="code"><div class="container"><div class="line number1 index0 alt2"><code class="py plain">move(item, parent, index)</code></div></div></td></tr></tbody></table>

Этот метод создает новый элемент и возвращает его идентификатор, который по умолчанию представляет строку наподобие "IOO1". Основные параметры метода:

-   item: идентификатор элемента, который надо переместить.
    
-   parent: представляет родительский элемент перемещаемого элемента .
    
-   index: индекс, на который перемещается элемент
    

#### Получение элементов

Для получения элементов применяется метод get\_children():

[?](https://metanit.com/python/tkinter/4.1.php#)

<table border="0" cellpadding="0" cellspacing="0"><tbody><tr><td class="gutter"><div class="line number1 index0 alt2">1</div></td><td class="code"><div class="container"><div class="line number1 index0 alt2"><code class="py plain">get_children(item)</code></div></div></td></tr></tbody></table>

Он принимает идентификатор элемента, дочерние элементы которого надо получить, и возвращает набор идентификаторов полученных элементов:

[?](https://metanit.com/python/tkinter/4.1.php#)

<table border="0" cellpadding="0" cellspacing="0"><tbody><tr><td class="gutter"><div class="line number1 index0 alt2">1</div></td><td class="code"><div class="container"><div class="line number1 index0 alt2"><code class="py keyword">for</code> <code class="py plain">k </code><code class="py keyword">in</code> <code class="py plain">treeview.get_children(""): </code><code class="py functions">print</code><code class="py plain">(k)</code></div></div></td></tr></tbody></table>

В данном случае k представляет идентификатор элемент.

В качестве параметра в `get_children()` передается элемент в Treeview, дочерние элементы которого мы хотим получить. Если надо получить элементы верхнего уровня (например, строки таблицы), то передается пустая строка.

Конкретный элемент по ключу с помощью метода item(), в который передается идентификатор элемента:

[?](https://metanit.com/python/tkinter/4.1.php#)

<table border="0" cellpadding="0" cellspacing="0"><tbody><tr><td class="gutter"><div class="line number1 index0 alt2">1</div><div class="line number2 index1 alt1">2</div></td><td class="code"><div class="container"><div class="line number1 index0 alt2"><code class="py keyword">for</code> <code class="py plain">k </code><code class="py keyword">in</code> <code class="py plain">treeview.get_children(""):</code></div><div class="line number2 index1 alt1"><code class="py spaces">&nbsp;&nbsp;&nbsp;&nbsp;</code><code class="py functions">print</code><code class="py plain">(treeview.item(k))</code></div></div></td></tr></tbody></table>

в данном случае `treeview.item(k)` возвратит набор значений элемента в Treeview (например, всю строку).

Если нам надо получить не весь набор значений, а только одно значение (отдельную ячейку строки), то применяется метод set(), в который передается идентификатор элемента и номер столбца:

[?](https://metanit.com/python/tkinter/4.1.php#)

<table border="0" cellpadding="0" cellspacing="0"><tbody><tr><td class="gutter"><div class="line number1 index0 alt2">1</div><div class="line number2 index1 alt1">2</div></td><td class="code"><div class="container"><div class="line number1 index0 alt2"><code class="py keyword">for</code> <code class="py plain">k </code><code class="py keyword">in</code> <code class="py plain">treeview.get_children(""):</code></div><div class="line number2 index1 alt1"><code class="py spaces">&nbsp;&nbsp;&nbsp;&nbsp;</code><code class="py functions">print</code><code class="py plain">(treeview.</code><code class="py functions">set</code><code class="py plain">(k, </code><code class="py value">0</code><code class="py plain">))</code></div></div></td></tr></tbody></table>

В данном случае получаем значение первой ячейки строки (при табличном отображении).

#### Изменение значений

Если надо изменить один столбец, то применяется метод set()

[?](https://metanit.com/python/tkinter/4.1.php#)

<table border="0" cellpadding="0" cellspacing="0"><tbody><tr><td class="gutter"><div class="line number1 index0 alt2">1</div></td><td class="code"><div class="container"><div class="line number1 index0 alt2"><code class="py functions">set</code><code class="py plain">(item, column, value)</code></div></div></td></tr></tbody></table>

-   item: идентификатор элемента, который надо изменить.
    
-   column: индекс элемента в кортеже (столбца в строке), который надо изменить.
    
-   value: новое значение
    

например:

[?](https://metanit.com/python/tkinter/4.1.php#)

<table border="0" cellpadding="0" cellspacing="0"><tbody><tr><td class="gutter"><div class="line number1 index0 alt2">1</div></td><td class="code"><div class="container"><div class="line number1 index0 alt2"><code class="py plain">treeview.</code><code class="py functions">set</code><code class="py plain">(</code><code class="py string">"I003"</code><code class="py plain">, </code><code class="py value">0</code><code class="py plain">, </code><code class="py string">"Admin"</code><code class="py plain">)</code></div></div></td></tr></tbody></table>

Здесь значение в первом столбце элемента с id=I003 меняется на строку "Admin"

Если надо изменить вообще весь элемент со всеми его значениями, то применяется метод item()

[?](https://metanit.com/python/tkinter/4.1.php#)

<table border="0" cellpadding="0" cellspacing="0"><tbody><tr><td class="gutter"><div class="line number1 index0 alt2">1</div></td><td class="code"><div class="container"><div class="line number1 index0 alt2"><code class="py plain">item(item, values)</code></div></div></td></tr></tbody></table>

-   item: идентификатор элемента, который надо изменить.
    
-   values: кортеж с новыми значениями
    

например:

[?](https://metanit.com/python/tkinter/4.1.php#)

<table border="0" cellpadding="0" cellspacing="0"><tbody><tr><td class="gutter"><div class="line number1 index0 alt2">1</div></td><td class="code"><div class="container"><div class="line number1 index0 alt2"><code class="py plain">treeview.item(</code><code class="py string">"I003"</code><code class="py plain">, values</code><code class="py keyword">=</code><code class="py plain">(</code><code class="py string">"Tim"</code><code class="py plain">, </code><code class="py value">34</code><code class="py plain">, </code><code class="py string">"tim@email.com"</code><code class="py plain">))</code></div></div></td></tr></tbody></table>

Здесь элемент с id=I003 в качестве значений принимает кортеж `("Tim", 34, "tim@email.com")`

В следующих статьях рассмотрим применение этих методов.