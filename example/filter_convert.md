
Examples of convert filter

Conversion functions are performed using the convert-units library.
[https://github.com/ben-ng/convert-units][md-convert-units].


### TEMPLATE
```
* Convert from liter to millilitre: **{{data.units.unit_less_1}} liter** is **{{data.units.unit_less_1 | Convert.FromTo('l','ml')}} millilitre**
* Convert from kilogramme to libre : **{{data.units.unit_more_1}} kg** is **{{data.units.unit_more_1 | Convert.FromTo('kg','lb') | round(4) }} libre**
* Convert from meters to kilometers : **{{data.units.unit_more_100}} meters** is **{{data.units.unit_more_100 | Convert.FromTo('m','km') | round(4) }} kilometers**
* Convert from Mb to Gb : **{{data.units.unit_more_1000}} Mb** is **{{data.units.unit_more_1000 | Convert.FromTo('Mb','Gb') | round(4) }} Gb**
* Convert from °F to °C : **{{data.units.unit_1 + 70}} °F** is **{{data.units.unit_1  + 70| Convert.FromTo('F','C') | round(2) }} °C**
 
 
```


### RESULT
* Convert from liter to millilitre: 0.543 liter is 543 millilitre
* Convert from kilogramme to libre : 1.232 kg is 2.7161 libre
* Convert from meters to kilometers : 123.093 meters is 0.1231 kilometers
* Convert from Mb to Gb : 1630.093 Mb is 1.5919 Gb
* Convert from °F to °C : 71 °F is 22.11 °C


###JSON snippet

```
 "units": {
    	    "unit_less_1" :0.543,
    	    "unit_1":1,
    	    "unit_more_1":1.232,
    	    "unit_more_100":123.093,
	       "unit_more_1000":1630.093
    	}

```
	 
	 
	 
	 
