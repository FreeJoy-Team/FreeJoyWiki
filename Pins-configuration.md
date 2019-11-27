Device pins can be configured is buttons (digital inputs) and analog inputs. Pins are configured in the "Pin Config" tab:

<img src="https://d.radikal.ru/d34/1911/ba/4aec9a66b7b0.png">

## Connection

Analog inputs can be connected to pins A0-A7. Digital pins can be connected to any of available pins.

There are three ways to connect digital inputs:
* Single buttons
* Matrix of buttons

### Connecting Single buttons

Single buttons can be connected as "active high" and "active low" buttons. The most common connection is "active low" when the first pin of button is connected to controller's pin and the second pin of button is connected to GND (shown at picture below)

<img src="https://c.radikal.ru/c13/1911/c5/6826d87c904a.png">

In this case select Button GND at expanding menu near needed pin.

<img src="https://c.radikal.ru/c03/1911/46/f4c4703f1e1d.png">

Controller will provide internal pull-up for chosen input and no external components are needed. 

In the other way the second pin on the button is connected to 3.3V, so Button VCC option must be selected. Controller will provide internal pull-down for selected pin

After setting up single buttons you will see its total count at "Current Config" panel:

<img src="https://b.radikal.ru/b08/1911/e9/10018e47dd2f.png">

### Connecting matrix of buttons 

In case of connecting buttons in matrix it is highly recommended to use schematic with diodes:

<img src="https://c.radikal.ru/c17/1911/9e/553f1f221bbd.png" height=400>

This will help to avoid negative affects at pushing several buttons at the same time.

For setting up buttons in a matrix select some pins of device as Rows and some as Columns:

<img src="https://a.radikal.ru/a43/1911/f0/e7ca5db4dbfe.png">

After setting up matrix buttons you will see total buttons count at "Current Config" panel:

<img src="https://d.radikal.ru/d26/1911/4f/bba505ec9957.png">

As you can see from the image above you can combine single and matrix buttons in your configuration.

  