1. Подключите программатор как показано на рисунке ниже (сверяйтесь с подписями контактов на программаторе и плате контроллера):

![](https://github.com/FreeJoy-Team/FreeJoyConfigurator//blob/master/images/rus_guide/1.jpg)

1. Подключите программатор ST-Link v2 к компьютеру;
1. Запустите программу ST-Link;
1. Нажмите в программе "File->Open File" и выберите файл с расширением .hex который расположен в архиве релиза FreeJoy;
1. Теперь вы увидите страницу загрузки бинарных кодов:

![](https://github.com/FreeJoy-Team/FreeJoyConfigurator/images/rus_guide/2.jpg)

1. Нажмите "Target->Connect". После подключения устройства вы можете видеть такую информацию как ID устройства, размер флэш-памяти и семейство устройства в блоке сверху и просмотреть содержимое внутренней памяти в основном блоке:

![](https://github.com/FreeJoy-Team/FreeJoyConfigurator/images/rus_guide/3.jpg)

1. Нажмите "Targert->Erase chip" и "OK" в открывшемся окне;

![](https://github.com/FreeJoy-Team/FreeJoyConfigurator/images/rus_guide/4.jpg)

1. Теперь нажмите "Target->Program & Verify" и в открывшемся окне нажмите "Start". Начнется программирование контроллера:

![](https://github.com/FreeJoy-Team/FreeJoyConfigurator/images/rus_guide/5.jpg)

1. После успешного программирования контроллера отключите все соединения и подключите плату контроллера к компьютеру посреством MicroUSB кабеля.
1. FreeJoy устройство определится в системе как игровой контроллер.
