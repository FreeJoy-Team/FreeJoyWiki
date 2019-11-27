FreeJoy supports up to 8 analog 12bit (4096 samples) inputs. Every analog input has such settings as:

* Calibration
* Invertion
* Smoothing
* Curve shaping

Settings for analog inputs are represented at "Axes Config" and "Axes Curves" tabs.

<img src="https://a.radikal.ru/a19/1911/da/702abddd2060.png">

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



### Automatic calibration

Is case of automatic calibration after startup the high limit is set to 0 and the low limit is set to 4095. Device is looking for lowest and highest values at analog input and set corresponding values to the limits. So if autocalibration is enabled you need to set the axis to the lowest position and then to the highest position after each startup. The center value will be calculated as (CalibMax-CalibMin)/2.