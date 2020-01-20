FreeJoy supports up to 128 digital inputs. Digital inputs are configured at "Button Config" tab.

<img src="https://a.radikal.ru/a42/1911/6c/76b195613953.png">

Before configuring digital inputs make sure the correct pins configuration is written to the device.

## Button mappings

By default all digital buttons set to Normal push button. 
Single buttons count starting from lowest number of pin at port A (A0, A1, A2...A7, B0, B1...). 
Buttons in matrix counted from first column and first row like this:

| Column Number | Row Number | Button Number |
| --- | --- | --- |
| Col 1 | Row 1 | Button 1 |
| Col 1 | Row 2 | Button 2 |
| --- | --- | --- |
| Col 1 | Row N | Button N |
| Col 2 | Row 1 | Button N+1 |
| Col 2 | Row 2 | Button N+2 |
| --- | --- | --- |
| Col M | Row N | Button N*M |

### Buttons priority

Buttons priority is (higher priority - lower number):

1. **Matrix buttons**
2. **Shift registers**
3. **Axes to buttons**
4. **Single buttons**

### Indication

If pin configuration is written to the device FreeJoy Configurator indicates when button is pushed by green background:

<img src="https://c.radikal.ru/c12/1911/0c/902081569054.png">

## Button configuration

Each digital input can be configured as:

| Input mode | Action |
|------------|--------|
| Normal push button | Logical high when pressed |
| Inverted push button | Logical low when pressed |
| Button toggle | Change logical state at press action |
| Toggle switch ON/OFF | Short press when state changes |
| Toggle switch ON | Short press when state changes from released to pressed |
| Toggle switch OFF | Short press when state changes from pressed to released |
| POV hat button left | POV |
| POV hat button right | POV |
| POV hat button up | POV |
| POV hat button down | POV |
| Incremental encoder input A | Short press at encoder step CW |
| Incremental encoder input B | Short press at encoder step CCW |

## Encoders

You can connect as many encoders as your digital pins allow. Both A and B encoder pin must be defined. In case of pin A defined an unused pin B with lowest number will be mapped to same encoder. Example (inputs with same color correspond same encoder):

<img src="https://a.radikal.ru/a20/1911/44/c7ad81d64a4e.png">

## Saving changes

For applying pins configuration and saving it to the device press button **"Write Config to Device"** and wait for **"Config Written"** message appeared:

<img src="https://d.radikal.ru/d33/2001/03/d9b2a553a823.png"/>