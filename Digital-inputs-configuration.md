FreeJoy supports up to 128 digital inputs. Each can be configured as:

* Regular push button
* Inverted push button
* Toggle switch ON/OFF
* Toggle switch ON
* Toggle switch OFF
* POV hat button
* Incremental encoder input

## Connection
Digital inputs can be connected to any pin available in the "Pin Config" tab:
<img src="https://d.radikal.ru/d34/1911/ba/4aec9a66b7b0.png">

There are two ways to connect digital inputs:
* Single buttons
* Matrix of buttons

In case of connecting buttons in matrix it is highly recommended to use schematic with diodes:
<img src="https://habrastorage.org/files/5b6/8bf/f0f/5b68bff0fcf043eaac33246af5320dd1.png" height=500>

This will help to avoid negative affects at pushing several buttons at the same time.


### Connecting Single buttons

Single buttons can be connected as "active high" and "active low" buttons. The most common connection is "active low" when the first pin of button is connected to controller's pin and the second pin of button is connected to GND (shown at picture below)
<img src="https://c.radikal.ru/c13/1911/c5/6826d87c904a.png">

In this case select Button GND at expanding menu near needed pin.
<img src="https://c.radikal.ru/c03/1911/46/f4c4703f1e1d.png">

Controller will provide internal pull-up for chosen input and no external components are needed. 
The other way the second pin on the button is connected to 3.3V, so Button VCC option must be selected. Controller will provide internal pull-down for selected pin

### Connecting matrix of buttons 

