Для получения прямого доступа к физическим USB устройствам компьютера из [подсистемы Windows для Linux](https://winitpro.ru/index.php/2020/07/13/zapusk-linux-v-windows-wsl-2/) (WSL2) или виртуальной машины Hyper-V вы можете open-source проект **usbipd-win**. Это проект позволяет настроить сквозную передачу внешнего USB устройства, подключенного к хостовой Windows, в любой дистрибутив Linux, запущенный в виде WSL или в виртуальные машины. Это позволяет выполнять любые действия с USB устройствами из Linux (прошивка Android устройств/ADB/Fastboot, доступ к смарт-картам, работа с оборудованием Arduino и т.д.).

В usbipd-win используется протокол USB/IP для перенаправления USB трафика через виртуальный сетевой интерфейс между WSL и хостовой Windows. Сначала мы настроим клиент USB/IP в Linux (WSL), и затем установим и установим и запустим серверную часть usbipd-win на Windows и прокинем USB устройство в Linux.

> Usbipd-win поддерживает версии, начиная с Windows 8.1 x64 и Windows Server 2012 R2, и позволяет предоставить общий доступ к локальным USB устройствам Windows другим виртуальным машинам (включая WSL2 и гостевые ОС Linux на Hyper-V). С помощью встроенных средств [Hyper-V ранее можно было пробрасывать только USB накопители](https://winitpro.ru/index.php/2014/06/26/kak-napryamuyu-probrosit-usb-disk-v-virtualnuyu-mashinu-hyper-v/) или другие виды USB устройства через довольно ограниченный режим Enhanced Session Mode.

Проект usbipd-win доступен на GitHub ([https://github.com/dorssel/usbipd-win](https://github.com/dorssel/usbipd-win)). Вы можете скачать и установить его вручную (доступен установочный MSI файл), но гораздо быстрее установить приложение с помощью [встроенного менеджера пакетов winget](https://winitpro.ru/index.php/2020/08/11/menedzher-paketov-winget-windows/).

`winget install --interactive --exact dorssel.usbipd-win`

Программа создаст в Windows отдельную службу usbipd (USBIP Device Host): `"C:\Program Files\usbipd-win\usbipd.exe" server,` которая слушает на порту TCP 3240

Для программы usbipd.exe в Windows Defender Firewall создано правило ( `usbipd` ), разрешающее доступ на порт TCP 3240 с компьютеров в локальной сети.

Теперь настроим поддержку USBIP в среде Windows Subsystem for Linux. Проверьте, что версия ядра в вашем образе не ниже 5.10.60.1 (в нашем примере для демонстрации используется WSL 2 с образом Ubuntu 22.04 LTS):

`$ uname -a`

Теперь нужно установить инструменты для работы с USB/IP и базу с идентификаторами USB устройств.

``$ sudo apt install linux-tools-virtual hwdata   $ sudo update-alternatives --install /usr/local/bin/usbip usbip `ls /usr/lib/linux-tools/*/usbip | tail -n1` 20``

> В Debian образе WSL используется команда:

> `$ sudo apt-get install usbip hwdata usbutils`  
> 
> Установка USB/IP утилит в WSL образа на базе rpm (CentOS/Oracle Linux):  
> `$ sudo rpm --import https://www.elrepo.org/RPM-GPG-KEY-elrepo.org   $ sudo rpm -ivh http://www.elrepo.org/elrepo-release-7.0-3.el7.elrepo.noarch.rpm   $ sudo yum install kmod-usbip   $ sudo yum install usbip-utils   $ sudo yum install hwdata`

Теперь откройте командную строку с правами администратора на хостовом Windows компьютере и выведите список USB устройств:

`usbipd wsl list`

Как вы видите, ни одно из USB устройств не опубликовано (Not shared). Вы можете предоставить общий доступ к USB устройству по его BUSID. В моем примере я хочу прокинуть в WSL флешку (USB Mass Storage Device) с BUISID 4-2.

`usbipd wsl attach --busid 4-2`

> - Если вы используете WSL 1 (не поддерживается в usbip), появится ошибка: _sbipd: error: The specified WSL distribution is using WSL 1, but WSL 2 is required. Learn how to upgrade at https://docs.microsoft.com/windows/wsl/basic-commands#set-wsl-version-to-1-or-2_.
> - Если появится ошибка: _usbipd: error: WSL kernel is not USBIP capable_, обновите WSL систему командой:  
    `wsl --update`

Проверьте, что ваша флешка была подключена к WSL:

`dmesg | tail   lsusb`

Если вы хотите прокинуть ваше USB устройство на другой компьютер с Linux ОС по сети (это может быть виртуальная машина с гостевой Linux на Hyper-V, или любом другом гипервизоре), сначала получить список опубликованных USB устройств:

`$ usbip list --remote=192.168.31.20`

Теперь можно подключить нужное USB по его ID:

`$ sudo usbip attach -remote=192.168.31.20 --busid=4-2`

В этом примере указан IP адрес хоста Windows, где запущен сервер usbipd-win.

Теперь ваши Linux утилиты должны увидеть подключенное USB устройство.

Чтобы отключить общий доступ к USB устройству в Windows:

`usbipd wsl detach --busid 4-2`

Обратите внимание, что подключенные таким образом USB накопители не определяются как блочные устройства в WSL. Проверьте это командой lsblk. Дело в том, что в ядре WSL отсутствует драйвера для USB накопителей (чтобы добавить их придется пересобрать ядро).

> В обычных дистрибутивах Linux вы сможете смонтировать файловую систему прокинутых USB накопителей стандартным образом.

Поэтому, если вам нужно смонтировать внешнюю USB флешку, диск, SD карту в WSL, нужно использовать такие команды:

`$ sudo mkdir /mnt/f   $ sudo mount -t drvfs f: /mnt/f`

> WSL может смонтировать таким образом диски с FAT, ExFAT, ReFs или NTFS, а также VHD образы.

Таким образом usbipd-win можно использовать для сквозной передачи физических USB устройств из Windows в WSL, в виртуальные машину или физические компьютер с Linux по сети с помощью USBOverIP

Также вам может быть полезна статья [по переносу WSL на другой диск](https://winitpro.ru/index.php/2022/01/10/wsl-perenos/).
