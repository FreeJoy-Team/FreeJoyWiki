For the quickstart you need the following tools and instruments:
* [BluePill board](https://camo.githubusercontent.com/a70b6639a020d201e1e1f0f582cd6374761a82d6/68747470733a2f2f642e726164696b616c2e72752f6433332f313931312f65382f6138666632313139636663372e6a7067)
* ST-Link v2 debugger or USB-UART converter
* [ST-Link Utility](https://www.st.com/en/development-tools/stsw-link004.html) (in case of ST-Link v2 debugger)
* [STM32 Flash loader demonstrator](https://www.st.com/en/development-tools/flasher-stm32.html) (in case of USB-UART converter)
* [Latest release](https://github.com/vostrenkov/FreeJoy/releases) of FreeJoy binaries

## Flashing software with ST-Link v2 debugger

* Connect ST-Link v2 to BluePill board as shown at picture below:

<img src="https://a.radikal.ru/a10/1911/2f/496ee3061643.jpg">

* Connect ST-Link v2 to your PC
* Run ST-Link Utility software
* Click **"File->Open File"** and select **hex** file of [latest FreeJoy release](https://github.com/vostrenkov/FreeJoy/releases). Yoy should now see page of loaded binaries:

<img src="https://b.radikal.ru/b31/1911/26/438741a2a25a.png" height=500>

* Click **"Target->Connect"**. After your device connect, you should see device info like device ID, flash size and device family in info block and internal memory view in main block:

<img src="https://b.radikal.ru/b31/1911/26/438741a2a25a.png" height=500>

* Click **"Targert->Erase chip"** and **"OK"** in appeared window:

<img src="https://c.radikal.ru/c03/2001/a9/9e466cce3105.png"/>

* Now click **"Target->Program & Verify"** and in appeared window press **"Start"**. The process of programming will now start:
<img src="https://a.radikal.ru/a36/1911/cb/567f4254d977.png">

* After successful programming unplug all connections and connect your BluePill device to your PC with an USB cable. 
* FreeJoy device should now appear in your system as a game controller:


## Flashing software with USB-UART converter

* Connect USB-UART converted to BluePill board as shown at picture below:

<img src="http://img.radiokot.ru/files/98849/medium/16s9sckulx.jpg">

* Set jumper for BOOT0 to 1 position:

<img src="https://forum.movimentomaker.pt/uploads/default/original/1X/d2fec4547aef853b6331c7b8323b3beb324bc3ba.jpg" height=400>

* Connect USB-UART converter to your PC
* Run STM32 Flash Loader Demonstrator software
* Choose COM port of your converter and press **"Next"** until you get to file dialog window
* Check **"Download to device"** and select hex file of latest FreeJoy release
* Press **"Next"** and wait flashing to finish
* Set BOOT0 jumper to 0 position and unplug all connections
* Connect your BluePill device to your PC with an USB cable. FreeJoy device should now appear in your system as a game controller.

## Configuration
After flash downloading FreeJoy device is set to its default configuration:

<img src="https://camo.githubusercontent.com/5af959eac151147ef76863218b14f2dc473e91d9/68747470733a2f2f612e726164696b616c2e72752f6132392f313830372f33622f3931316235383635346162372e6a7067">

You can change this configuration and map other functions to the device pins. The easiest way to configure your device is using [FreeJoy Configurator](https://github.com/vostrenkov/FreeJoyConfigurator) tool. Download its [latest release](https://github.com/vostrenkov/FreeJoyConfigurator/releases) and check [wiki page](https://github.com/vostrenkov/FreeJoyConfigurator/wiki) for detailed information. 