There are some setting for HID interface:

<img src="https://b.radikal.ru/b07/2002/ae/193afebe2ea8.png">

* Dynamic HID config checkbox. Not used axes and buttons will be removed from HID descriptor if checked
* **VID** number is static and can not be modified
* **PID** number can be changed if needed. For example if two **different** FreeJoy devices should be connected to the same PC (joystick and pedals for example). Each FreeJoy device has unique serial number so there is no need to change PID for several devices of same type.