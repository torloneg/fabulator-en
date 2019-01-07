Examples of date and time transformation

 
### TEMPLATE
```
random array int : {{ [1,2,3,4,5,6,7,8,9] | random }}

random array string : {{ data.array| random }}

test array all=1 : {{ data.array_1 | Array.allValuesSame }}

test array not all=1 : {{ data.array_1_0 | Array.allValuesSame }}

test array all=2 : {{ data.array_2 | Array.allValues(2) }}

test array not all=2 : {{ [2,2,2,0]| Array.allValues(2) }}

test array index =0 : {{ [2,2,2,0]| Array.Index(0) }}

test array index =10 : {{ [2,2,2,0]| Array.Index(10) }}


```


### RESULT
random array int : 8

random array string : second

test array all=1 : true

test array not all=1 : false

test array all=2 : true

test array not all=2 : false

test array index =0 : 2

test array index =10 :



###JSON snippet

```
 "array_1": [1,1,1,1,1,1	],
	"array_1_0": [1,1,1,1,1,0],
	"array_0": [0,0,0,0,0,0],
	"array_0_1": [0,0,0,0,0,1],
	"array_2": [2,2,2,2,2],
	"array_number": [1,2,3,4,5,6,7,8,9,10],
	"array": ["first","second",	"third","fourth","fifth"]

```
	 
	 
	 
	 
