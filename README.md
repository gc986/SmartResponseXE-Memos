# SmartResponseXE-Memos
<h2>Мои заметки по SmartResponseXE</h2>

Чем интересено это устройство? Тем что построено на основе микроконтроллера ATmega128RFA1, у него есть встроенная клавиатура и замечательный монохромный дисплей. А чем же интересен микроконтроллер (<i>ATmega128RFA1</i>)? Он имеет встроенный передатчик работающий по стандарту ZigBee. И к тому же, эти железки (<i>SmartResponseXE</i>) есть в асортименте на Ebay, т.к. в своё время их закупали в больших количествах в школы, а сейчас продают по 10$ за пару штук.


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

<h1>Переделка SmartResponseXE в Arduino-SmartResponseXE</h1>
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


