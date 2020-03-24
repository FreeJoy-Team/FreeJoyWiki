## Welcome to the FreeJoyConfigurator wiki!

<details> 
  <summary> English guide </summary>

# Installation
Just download the [latest release](https://github.com/FreeJoy-Team/FreeJoy/releases) and run the installer.

# Getting started
* [Pins configuration](https://github.com/vostrenkov/FreeJoyConfigurator/wiki/Pins-configuration)
* [Digital inputs (buttons) configuration](https://github.com/vostrenkov/FreeJoyConfigurator/wiki/Digital-inputs-configuration)
* [Axes configuration](https://github.com/vostrenkov/FreeJoyConfigurator/wiki/Axes-configuration)
* [Axes to buttons](https://github.com/vostrenkov/FreeJoyConfigurator/wiki/Axes-to-Buttons)
* [Shift registers](https://github.com/vostrenkov/FreeJoyConfigurator/wiki/Shift-registers)
* [TLE501x sensors](https://github.com/vostrenkov/FreeJoyConfigurator/wiki/TLE501x-sensors)
* [LED configuration](https://github.com/FreeJoy-Team/FreeJoyConfigurator/wiki/LED-configuration)
* [Loading and saving configuration](https://github.com/vostrenkov/FreeJoyConfigurator/wiki/Loading-and-saving-configuration)
* [Advanced settings](https://github.com/vostrenkov/FreeJoyConfigurator/wiki/Advanced-settings)
* [Firmware flasher](https://github.com/vostrenkov/FreeJoyConfigurator/wiki/Firmware-flasher)

</details>

<details> 
  <summary> Инструкция на русском (в разработке) </summary>

# Описание проекта:
# FreeJoy
FreeJoy - настраиваемый контроллер игрового устройства, основанный на недорогом микроконтроллере STM32F103C8. Он позволяет создавать собственные HOTAS – системы (РУС, РУД, всевозможные панели расширения), педали, автомобильные системы управления (рулевые колеса, педали, рычаги коробок передач и т.д.) и настраивать сконструированное устройство.

## Возможности:
* До 8 – аналоговых осей;
* До 128 кнопок или тумблеров;
* До 4 HAT-переключателей;
* До 16 инкрементальных энкодеров;
* Возможность назначения нажатий кнопок на определенные положения аналоговой оси (до 12 кнопок на ось);
* Поддержка сдвиговых регистров 74HC165 и CD4021 для увеличения количества подключаемых кнопок.
* Поддержка цифровых датчиков Холла TLE5010/TLE5011.

## Оси:
FreeJoy поддерживает до 8 аналоговых осей, которые могут быть либо аналоговыми источниками (потенциометрами) подключенными к контактам A0-A7, либо цифровыми (TLE5010/5011). Все оси имеют следующие настройки:
* Источник/назначение оси (X, Y, Z, Rx, Ry, Rz, Slider1, Slider2);
* Включение/отключение вывода оси;
* Изменение разрешения;
* Калибровка (ручная/автоматическая);
* Сглаживание (откл или 7 уровней настройки фильтра);
* Инверсия;
* Динамическая мертвая зона
* Опция сдвига магнита;
* Настройка кривых отклика;
* Оси из кнопок/энкодеров.

## Кнопки:
FreeJoy – поддерживает подключение до 128 кнопок поключенных как одиночные кнопки (подкача 0 или питания на сигнальный контакт), как матрица кнопок, посредством сдвиговых регистров, через функцию ось в кнопки. Кнопки могут быть настроены как:
* Нормальная кнопка;
* Инвертированная кнопка;
* Тумблер на включение/отключение (Toggle switch ON/OFF);
* Тумблер на включение (Toggle switch ON);
* Тумблер на отключение (Toggle switch OFF);
* HAT-переключатель;
* Вход инкрементального энкодера;
* Радиокнопка;
* Кнопка последовательного переключения;
* 5 шифтов.


Скачайте [последний релиз](https://github.com/FreeJoy-Team/FreeJoy/releases) и запустите установщик.

# Начало работы
* [Настройка выводов контроллера](https://github.com/FreeJoy-Team/FreeJoyConfigurator/wiki/Настройка-выводов-контроллера)
* [Настройка цифровых входов (кнопок)](https://github.com/FreeJoy-Team/FreeJoyConfigurator/wiki/Настройка-цифровых-входов-(кнопок))
* [Настройка осей](https://github.com/FreeJoy-Team/FreeJoyConfigurator/wiki/Настройка-осей)
* [Функция "оси в кнопки"](https://github.com/FreeJoy-Team/FreeJoyConfigurator/wiki/Функция-%22оси-в-кнопки%22)
* [Сдвиговые регистры](https://github.com/FreeJoy-Team/FreeJoyConfigurator/wiki/Сдвиговые-регистры)
* [Датчики TLE501x](https://github.com/FreeJoy-Team/FreeJoyConfigurator/wiki/Датчики-TLE501x)
* [Настройка светодиодов](https://github.com/FreeJoy-Team/FreeJoyConfigurator/wiki/Настройка-светодиодов)
* [Загрузка и сохранение конфигурации](https://github.com/FreeJoy-Team/FreeJoyConfigurator/wiki/Загрузка-и-сохранение-конфигурации)
* [Продвинутые настройки](https://github.com/FreeJoy-Team/FreeJoyConfigurator/wiki/Продвинутые-настройки)
* [Загрузчик прошивки](https://github.com/FreeJoy-Team/FreeJoyConfigurator/wiki/Загрузчик-прошивки)

</details>


### References
Thanks to [OpenSimHardware](https://github.com/OpenSimHardware) with [Pedal & Button Controller](https://github.com/OpenSimHardware/PedalButtonController) project for the idea and the inspiration.