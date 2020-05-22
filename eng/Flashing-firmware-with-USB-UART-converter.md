1. Connect the converter as shown in the figure below:

![](../images/6.jpg)

2. Set the BOOT0 jumper to position 1:

![](../images/7.jpg)

3. Plug the USB-UART converter into USB port.
4. Run the program STM32 Flash Loader Demonstrator.
5. Select the COM port that was assigned to your converter (the port number can be viewed in the device manager “Ports (COM and LPT)” and click “Next”:

![](../images/8.png)

5.1. If device protection is enabled click "Remove protection". Otherwise just press "Next" until you reach programming method window:

![](../images/9.png)

6. Click "Download to device" and select the .hex file which is located in the FreeJoy release archive. Aslo check option "Global erase":

![](../images/10.png)

7. Click “Next” and wait for the end of programming the controller.
8. Set the BOOT0 jumper to position 0 and disconnect all connections.
9. Connect the controller board to the computer using the microUSB cable. A FreeJoy device is defined in the system as a game controller.
