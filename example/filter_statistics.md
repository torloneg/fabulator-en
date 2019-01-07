Examples of statistical filter  using the convert-units library.
[https://simplestatistics.org/][md-statistical-simple].

### TEMPLATE
```
 MIN : minimum of {{data.array_number | dump }} is **{{data.array_number | Stats.Min}}**
 
 MAX :  maximum of {{data.array_number | dump }} is **{{data.array_number | Stats.Max}}**
 
 SUM : the sum of the values  {{data.array_number | dump }} is **{{data.array_number | Stats.Sum}}**
 
 MEAN : {{data.array_number | Stats.Mean}}
 MEDIAN : {{data.array_number | Stats.Median}}
 
 
```


### RESULT
MIN : minimum of [1,2,3,4,5,6,7,8,9,10] is 1

MAX : maximum of [1,2,3,4,5,6,7,8,9,10] is 10

SUM : the sum of the values [1,2,3,4,5,6,7,8,9,10] is 55

MEAN : 5.5

MEDIAN : 5.5



###JSON snippet

```
"array_number": [1,2,3,4,5,6,7,8,9,10]

```
	 
	 
	 
	 
