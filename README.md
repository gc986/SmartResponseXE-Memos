# SmartResponseXE-Memos

<h1>Оглавление</h1>
<ul>
  <li><a href="#about">Краткое описание SmartResponseXE</a>
  <li><a href="#links">Ссылки/Документация</a>
  <li><a href="#remake-terminal">Переделка SmartResponseXE в Arduino-SmartResponseXE</a>
  <li><a href="#connecting-spi">Подключение к ISP (загрузка прошивки)<a>
  <li><a href="#no-access-linux-avr-dude">Нехватка прав при попытке прошить плату в Linux с помощью avrdude</a>
  <li><a href="#features-terminal-smart-response-xe">Особенности технической реализации SMART Response XE</a>
</ul>



<h2><a name="about">Краткое описание SmartResponseXE</a></h2>

Чем интересено это устройство? Тем что построено на основе микроконтроллера ATmega128RFA1, у него есть встроенная клавиатура и замечательный монохромный дисплей. А чем же интересен микроконтроллер (<i>ATmega128RFA1</i>)? Он имеет встроенный передатчик работающий по стандарту ZigBee. И к тому же, эти железки (<i>SmartResponseXE</i>) есть в асортименте на Ebay, т.к. в своё время их закупали в больших количествах в школы, а сейчас продают по 10$ за пару штук.

<a name="links"><h2>Ссылки/Документация</h2></a>
Схемы добытые путём реверс инженеренгом и зоркими глазами - https://github.com/fdufnews/SMART-Response-XE-schematics

<b>Оригинальный datasheet на чип ATmega128RFA1 (5mb!) - https://github.com/gc986/SmartResponseXE-Memos/blob/main/docs/ATmega128RFA1_Datasheeta.pdf</b>

<b>SparkFun</b>
<ul>
  <li>Загрузчик взят из проекта SparkFun "ATmega128RFA1 Dev Board" - https://cdn.sparkfun.com/assets/learn_tutorials/9/2/ATmega128RFA1_Addon.zip
  (копия в текущем репозиторий "archives/bootloader-ATmega128RFA1_Addon.zip")</li>
  <li>Страница с настройками Arduino - https://learn.sparkfun.com/tutorials/atmega128rfa1-dev-board-hookup-guide#example-code
  (копия в текущем репозитории "docs/sparkfun_com_tutorials_atmega128rfa1_dev_board.pdf")</li>
  <li>Оригинальный репозиторий проекта - https://github.com/sparkfun/ATmega128RFA1_Dev</li>
</ul>


Репозиторий для Arduino, по управлению клавиатурой и экраном для SmartResponseXE - https://github.com/bitbank2/SmartResponseXE
(копия в текущем репозитории "archive/SmartResponseXE-master.zip")

<a name="remake-terminal"><h2>Переделка SmartResponseXE в Arduino-SmartResponseXE</h2></a>
Чтобы переделать терминал сбора данных SmartResponseXE в Arduino, нужно немного доработать само ус-во (вывести на ружу порты для программирования платы), и залить загрузчик. После этого, ус-во будет вести себя как обычный прокаченный Arduino, с дисплеем, клавиатурой и беспроводным интерфейсом.

Ниже приведёна последовательность разбора устройства. Устройство собрано на редкость хорошо, все пазы на месте, прямо такое антивандальное ус-во для использования в школах. Теме не менее будьте аккуратны при разборе, и не забудьте про винтик под батарейным блоком:


1<br>
<img src="https://github.com/gc986/SmartResponseXE-Memos/blob/main/images/disassembling-1.jpg">

2<br>
<img src="https://github.com/gc986/SmartResponseXE-Memos/blob/main/images/disassembling-2.jpg">

3<br>
<img src="https://github.com/gc986/SmartResponseXE-Memos/blob/main/images/disassembling-3.jpg">

4<br>
<img src="https://github.com/gc986/SmartResponseXE-Memos/blob/main/images/disassembling-4.jpg">

5<br>
<img src="https://github.com/gc986/SmartResponseXE-Memos/blob/main/images/disassembling-5.jpg">

6<br>
<img src="https://github.com/gc986/SmartResponseXE-Memos/blob/main/images/disassembling-6.jpg">

7<br>
<img src="https://github.com/gc986/SmartResponseXE-Memos/blob/main/images/disassembling-7.jpg">

8<br>
<img src="https://github.com/gc986/SmartResponseXE-Memos/blob/main/images/disassembling-8.jpg">

9<br>
<img src="https://github.com/gc986/SmartResponseXE-Memos/blob/main/images/disassembling-9.jpg">

10<br>
<img src="https://github.com/gc986/SmartResponseXE-Memos/blob/main/images/disassembling-10.jpg">


<a name="connecting-spi"><h2>Подключение к ISP (загрузка прошивки)</h2></a>
Для загрузки прошивки в микроконтроллер терминала, я пользуюсь страндартным интерфейсом ISP. Для него вынесена специальная площадка для подключения. Для удобства работы с интерфейсом,я предлагаю подпаять провода для дальнейшего подключения к программатору.
<br>
<img src="https://github.com/gc986/SmartResponseXE-Memos/blob/main/images/ISP-0.jpg">

<br>
Для подключения и использую стандартные провода для макетирования, предварительно отрезав крайнюю часть. Очень удобно что в корпусе терминала есть технологические отверстия. В них удобно протянуть провода и закрутить в узел чтобы в дальнейшем они не имели шанс быть выдернутыми.
<br>
<img src="https://github.com/gc986/SmartResponseXE-Memos/blob/main/images/ISP-1.jpg">
<br>
<img src="https://github.com/gc986/SmartResponseXE-Memos/blob/main/images/ISP-2.jpg">


После того как вы припаяите провода, у вас может получиться следующий результат:
<br>
<img src="https://github.com/gc986/SmartResponseXE-Memos/blob/main/images/ISP-3.jpg">


<a name="no-access-linux-avr-dude"><h2>Нехватка прав при попытке прошить плату в Linux с помощью avrdude</h2></a>

Если при попытке прошить SmartResponseXE в Linux с помощью avrdude вы сталкиваетесь с ошибкой нехватки прав:

<i><b>avrdude: usbdev_open(): cannot open device: Permission denied</b></i>

То вам помогут вот эти команды:

<i><b>echo "SUBSYSTEM==\\"usb\\", MODE=\\"0660\\", GROUP=\\"$(id -gn)\\"" | sudo tee /etc/udev/rules.d/00-usb-permissions.rules
<br>
sudo udevadm control --reload-rules</b></i>

! Переподключите программатор/устройство и только после этого новые правила вступят в силу !

Данные команды делает вашего пользователя Linux неограниченным пользователем USB устройств. С точки зрения безопасности это плохо, так как любой код запущенный от вашего имени будет иметь неограниченный доступ к USB устройствам, но с другой стороны ничего лучше не получилось сделать, так как разработчики avrdude работают с данными USB устройства напрямую, в обход стандартного протокола работы с USB. (оригинал https://github.com/snapcrafters/arduino/issues/10)


<a name="#features-terminal-smart-response-xe"><h2>Особенности технической реализации SMART Response XE</h2></a>
Нога пятого столбца клавиатуры (клавиши 5, T, G, V), подключены на порт реализующий интерфейс подключения UART, поэтому одновременное использование UART и клаиватуры невозможно в нормальном режиме (при нажатии на клавиши пятого столбца будут происходить сробатывания десятого ряда клавиатуры, например при нажатии на клавишу T, систему будет определять что нажата клавиша P)
