FreeJoy supports up to 128 digital inputs. Each can be configured as:

* Normal push button
* Inverted push button
* Button toggle
* Toggle switch ON/OFF
* Toggle switch ON
* Toggle switch OFF
* POV hat button
* Incremental encoder input

Digital inputs are configured at "Button Config" tab.

<img src="https://a.radikal.ru/a42/1911/6c/76b195613953.png">

Before configuring digital inputs make sure the correct pins configuration is written to the device.

## Configuring buttons

By default all digital buttons set to Normal push button. 
Single buttons count starting from lowest number of pin at port A (A0, A1, A2...A7, B0, B1...). 
Buttons in matrix counted from first column and first row like this:

| Column Number | Row Number | Button Number |
| --- |  |  |
| Col 1 | Row 1 | Button 1 |
| Col 1 | Row 2 | Button 2 |
| --- | |  |
| Col 1 | Row N | Button N |
| Col 2 | Row 1 | Button N+1 |
| Col 2 | Row 2 | Button N+2 |
| --- |  |  |
| Col M | Row N | Button N*M |