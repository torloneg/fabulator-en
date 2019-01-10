---
description: Description of Convert
---

# Convert


## Convert.FromTo
A handy utility for converting between quantities in different units.


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | float  | 
    | from | string  | 
    | to | string  | 

```
example: {{  1 | Convert.FromTo('l','ml')}}

output: 1000

```
---
```
Length : mm, cm, m, in, ft-us, ft, mi
Area: mm2, cm2, m2, ha, km2, in2, ft2, ac, mi2
Mass: mcg, mg, g, kg, oz, lb, mt, t
Volume: mm3, cm3 ml, l, kl, m3, km3, tsp, Tbs,  in3, fl-oz,cup, pnt, qt, gal, ft3, yd3
Temperature: C, F, K ,R
Time: ns, mu, ms, s, min, h, d, week, month, year
Frequency: Hz, mHz, kHz, MHz, GHz, THz, rpm, deg/s, rad/s
Speed: m/s, km/h, m/h, knot, ft/s
Pressure: Pa, hPa, kPa, MPa, bar, torr, psi, ksi
Digital: b, Kb, Mb, Gb, Tb, B, KB, MB, GB, TB
Voltage: V, mV, kV
Current: A, mA, kA
Power: W, mW, kW, MW, GW
Energy: Wh, mWh, kWh, MWh, GWh, J, kJ
Angle: deg, rad, grad, arcmin, arcsec
Force: N, kN, lbf

```


