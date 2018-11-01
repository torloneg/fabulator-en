---
description: Description of DateTime
---

# Moment


## Moment.AgeDays
numbers of days elapsed between the input date and today


**params**
    |  |  |
    | :--- | :--- |


```
example: {{"31/10/2018" |Moment.AgeDays()}}

output: 30

```
## Moment.AgeYear
numbers of years elapsed between the input date and today


**params**
    |  |  |
    | :--- | :--- |


```
example: {{"31/10/2000" |Moment.AgeYear()}} {{"31/10/2017" |Moment.AgeYear()}}

output: 18
1

```
## Moment.Now
Now in format string


**params**
    |  |  |
    | :--- | :--- |
    | title | language  |
    | type | string |
    | value |  |
    | title | format  |
    | type | string |
    | value |  |


```
example: {{"" |Moment.Now('it','DD/MM/YYYY hh:mm:ss')}} {{"" |Moment.Now('it','DD MMM YYYY')}}

output: 31/10/2018 22:22:22
31 Ottobre 2018

```


