FreeJoy supports up to 8 analog 12bit (4096 samples) inputs. Every analog input has such settings as:

* Calibration
* Invertion
* Smoothing
* Curve shaping

Settings for analog inputs are represented at "Axes Config" and "Axes Curves" tabs.

<img src="https://a.radikal.ru/a19/1911/da/702abddd2060.png">

Before axis configuration you should be sure the correct pins for analog inputs are chosen in "Pin Config" tab and configuration is written to the device.

## Calibration

By default all inputs calibrated to fullscale range 0-4095. You can choose one of two options for calibration:

* Manual calibration
* Automatic calibration

For axes calibration calibration go to "Axis Config" tab. You will see 8 blocks for 8 analog inputs where 1st is mapped to the lowest number of pin at A port (A0 by default). 

### Manual calibration

In case of manual calibration set your axis to the lowest position and set the "Minimum" value to the current Raw value:

<img src="https://b.radikal.ru/b10/1911/c3/406ffb262d3f.png">

Then set set axis to the highest position and set "Maximum" value to the current Raw value:

<img src="https://d.radikal.ru/d42/1911/8d/bfb073aa2eed.png">

In case you have asymmetrical axis input you can set center position. Do do this you need to check Center checkbox, set your axis to the neutral position and set "Center" value to current Raw value:

<img src="https://b.radikal.ru/b28/1911/e3/157b586a1906.png">

After writing config to the device you will see that device now scaling input data to the lower and higher limits and logical center corresponds the physical neutral position:

<img src="https://a.radikal.ru/a36/1911/6b/d7a48d7ec165.png">

### Automatic calibration

Is case of automatic calibration after startup the high limit is set to 0 and the low limit is set to 4095. Device is looking for lowest and highest values at analog input and set corresponding values to the limits. So if autocalibration is enabled you need to set the axis to the lowest position and then to the highest position after each startup. The center value will be calculated as (CalibMax-CalibMin)/2.
For enabling automatic calibration check "Autocalibration" checkbox for the corresponding axis.

## Invertion

Every axis can be logically inverted by checking "Inverted" checkbox for corresponding axis

## Smoothing

You can set smoothing for every axis by dragging "Smoothing" slider. There are 4 levels of smoothing:

* Off
* Low
* Medium
* High

## Curve shaping

You can set a custom curve shape for every axis. This settings and represented at "Axes Curves" tab:

<img src="https://d.radikal.ru/d20/1911/ed/b4a208040b8c.png">

There are 10 points you can drag for setting the custom curve shape:

<img src="https://d.radikal.ru/d23/1911/13/b5d81f378bd1.png">

For your convenience there are 4 presets available. To apply the preset just press on it: 

<img src="https://d.radikal.ru/d40/1911/23/26150c28d8d1.png">

  