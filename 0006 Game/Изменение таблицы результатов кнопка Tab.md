Если вы хотите изменить цвета живых и мёртвых игроков, а так же клан-тега в окне таблицы счёта игроков (кнопка TAB), вам рекомендуется полностью прочесть это руководство и сделать всё по инструкции.

  
**Для примера приведу свою немного переделанную таблицу счёта.  
Я сделал себе выделяющиеся розовые клан-теги, так же немного ярче цвета никнеймов выглядят у игроков за T и CT, мёртвых игроков Я чуть-чуть затемнил.**  
[![](https://steamuserimages-a.akamaihd.net/ugc/903251184099963525/6CC95EA262A5CCD98D71D19356C23B837B8DC034/)](https://steamuserimages-a.akamaihd.net/ugc/903251184099963525/6CC95EA262A5CCD98D71D19356C23B837B8DC034/)

Стандартные цвета / Default scoreboard colors

Цвет никнеймов игроков за спецназ / Alive CT nicknames

cl\_scoreboard\_ct\_color\_red "150"  
cl\_scoreboard\_ct\_color\_green "200"  
cl\_scoreboard\_ct\_color\_blue "255"  
  

Цвет никнеймов игроков за террористов / Alive T nicknames

cl\_scoreboard\_t\_color\_red "240"  
cl\_scoreboard\_t\_color\_green "90"  
cl\_scoreboard\_t\_color\_blue "90"  
  

Цвет никнеймов мёртвых игроков / Dead players nickname color

cl\_scoreboard\_dead\_color\_red "125"  
cl\_scoreboard\_dead\_color\_green "125"  
cl\_scoreboard\_dead\_color\_blue "125"  
  

Цвет клан-тега игроков за спецназ / Clan-Tag for CT players

cl\_scoreboard\_clan\_ct\_color\_red "150"  
cl\_scoreboard\_clan\_ct\_color\_green "200"  
cl\_scoreboard\_clan\_ct\_color\_blue "255"  
  

Цвет клан-тега игроков за террористов / Clan-Tag for T players

cl\_scoreboard\_clan\_t\_color\_red "240"  
cl\_scoreboard\_clan\_t\_color\_green "90"  
cl\_scoreboard\_clan\_t\_color\_blue "90"  
  

Цвет клан-тега мёртвых игроков / Clan-Tag for dead players

cl\_scoreboard\_dead\_clan\_color\_red "125"  
cl\_scoreboard\_dead\_clan\_color\_green "125"  
cl\_scoreboard\_dead\_clan\_color\_blue "125"  
  
Выше преведены _**стандартные цвета**_ таблицы счёта. / This is default settings for scoreboard.  
Для изменения своей таблицы вам необходимо составить для себя свой цвет определённого или всех параметров (используется цветовая модель RGB) и _внести их в файл autoexec.cfg_, который надо создать по такому адресу: **Диск:\\Steam\\steamapps\\common\\Counter-Strike Source\\cstrike\\custom\\my\_custom\_stuff\\cfg\\autoexec.cfg  
  
To customize your scoreboard, you need to make for yourself your specified color parameters (color model used RGB) and _put config with colors in file autoexec.cfg_ in the folder: **Steam\\steamapps\\common\\Counter-Strike Source\\cstrike\\custom\\my\_custom\_stuff\\cfg**  
  
**Большую базу **RBG** цветов Вы можете найти на следующих сайтах: (кликабельные ссылки / clickable links for RGB colors)  

-   [Яндекс "RGB"](https://steamcommunity.com/linkfilter/?url=http://yandex.ru/yandsearch?clid=9582&text=%D1%8F%D0%BD%D0%B4%D0%B5%D0%BA%D1%81+rgb&lr=54)\[yandex.ru\]  
    
-   [RGB to Color Name Mapping (Triplet and Hex)](https://steamcommunity.com/linkfilter/?url=http://web.njit.edu/~kevin/rgb.txt.html)\[web.njit.edu\]  
    
-   [RGB Color Wheel](https://steamcommunity.com/linkfilter/?url=http://www.colorspire.com/rgb-color-wheel/)\[www.colorspire.com\]

**  
**

Полное изменение таблицы счёта (пример) / Full customization scoreboard (example)

Давайте попробуем полностью разукрасить таблицу счёта игроков.

[![](https://steamuserimages-a.akamaihd.net/ugc/903251184100341986/6414BF06E079A014EAA374F3B61418B1448E20EE/)](https://steamuserimages-a.akamaihd.net/ugc/903251184100341986/6414BF06E079A014EAA374F3B61418B1448E20EE/)  
**Вот так выглядят параметры для вышепоказанной таблицы.**  
_cl\_scoreboard\_ct\_color\_red "46"  
cl\_scoreboard\_ct\_color\_green "222"  
cl\_scoreboard\_ct\_color\_blue "242"  
cl\_scoreboard\_t\_color\_red "235"  
cl\_scoreboard\_t\_color\_green "180"  
cl\_scoreboard\_t\_color\_blue "70"  
cl\_scoreboard\_dead\_color\_red "249"  
cl\_scoreboard\_dead\_color\_green "239"  
cl\_scoreboard\_dead\_color\_blue "230"  
cl\_scoreboard\_clan\_ct\_color\_red "245"  
cl\_scoreboard\_clan\_ct\_color\_green "16"  
cl\_scoreboard\_clan\_ct\_color\_blue "245"  
cl\_scoreboard\_clan\_t\_color\_red "42"  
cl\_scoreboard\_clan\_t\_color\_green "238"  
cl\_scoreboard\_clan\_t\_color\_blue "28"  
cl\_scoreboard\_dead\_clan\_color\_red "247"  
cl\_scoreboard\_dead\_clan\_color\_green "247"  
cl\_scoreboard\_dead\_clan\_color\_blue "12"_  
  

Если кому понравилась моя таблица, держите мои значения.

This is my configuration (see 1st picture).

_cl\_scoreboard\_ct\_color\_red "3"  
cl\_scoreboard\_ct\_color\_green "180"  
cl\_scoreboard\_ct\_color\_blue "200"  
cl\_scoreboard\_t\_color\_red "255"  
cl\_scoreboard\_t\_color\_green "36"  
cl\_scoreboard\_t\_color\_blue "0"  
cl\_scoreboard\_dead\_color\_red "78"  
cl\_scoreboard\_dead\_color\_green "78"  
cl\_scoreboard\_dead\_color\_blue "78"  
cl\_scoreboard\_clan\_ct\_color\_red "238"  
cl\_scoreboard\_clan\_ct\_color\_green "130"  
cl\_scoreboard\_clan\_ct\_color\_blue "238"  
cl\_scoreboard\_clan\_t\_color\_red "238"  
cl\_scoreboard\_clan\_t\_color\_green "130"  
cl\_scoreboard\_clan\_t\_color\_blue "238"  
cl\_scoreboard\_dead\_clan\_color\_red "78"  
cl\_scoreboard\_dead\_clan\_color\_green "78"  
cl\_scoreboard\_dead\_clan\_color\_blue "78"_