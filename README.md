# Управление адресной лентой ws2812b с помощью ESP8266 через web интерфэйс
![scheme](http://www.imageup.ru/img152/3333632/p111005.jpg)
## Описание проекта
##### Управление:
* По WiFi или по Ethernet порту

##### Особенности:
- Постоянное TCP соединение
- Длительность срабатывания при наихудшем сигнале WiFi не более 500мс 
- Возможность асинхронного управления
- Удобный colorpicker [от автора](https://github.com/NC22/HTML5-Color-Picker)
- Имееться **29**  крутых эффектов
- Плавная смена цветов
- Плавная регулировка яркости

## Материалы и компоненты
- ESP8266
- ws2812b
- резистор от перегрузки пина ESP (желательно)
- 5-вольтовый источник питания (емкость в зависимости от кол-ва пикселей в ленте)
- провода перемычки
- Один из последних версий Arduino IDE вместе с :
   - [Пакеты для ESP8266](https://github.com/esp8266/Arduino)
   - [ESP8266FS плагин файловой системы](https://github.com/esp8266/arduino-esp8266fs-plugin) (используется для загрузки HTML, JS, CSS файлов в ESP)
    - Библиотека Websockets (доступно из менеджера библиотек)
    - Библиотека FastLed (доступно из менеджера библиотек)
## Схема подключения
![scheme](http://ipic.su/img/img7/fs/espscheme.1543413145.png)
## Установка
- Подключить ESP8266 к вашему компьютеру
- Открыть `ESP8266-LED.ino` и обновить сетевые настройки для вашей сети 
- Загрузить скетч
- В верхнем меню IDE выберите инструменты - > ESP8266 Sketch Upload, чтобы загрузить веб-файлы из каталога `data`.
- Откройте монитор последовательного порта (при успешном подключении отобразиться ваш IP).
- Перейдите по IP-адресу и наслаждайтесь )

## Aхтунг !
![button](http://www.imageup.ru/img25/3225651/dan.png)
Отмеченные функции с данным окрасом, имеют длинный цикл и при быстром смене яркости ESP8266 сильно нагружается и могут наблюдаться задержки !
Рекомендую перед использованием этих функций сначала установить яркость.
