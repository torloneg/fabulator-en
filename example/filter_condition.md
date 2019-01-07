## CONDITION

These functions allow you to toggle natural language text based on the content of values 

 
## TEMPLATE
```
Condition on number : {{ data.number | Condition.Value([{value:0,text:'zero'},{value:1,text:'one'},{value:2,text:'two'},{value:3,text:'three'}]) }}

Condition on range : {{ 1 | Condition.Range([{value:'0|5',text:'from 1 to 5'},{value:'6|10',text:'from six to ten'},{value:'11|1000',text:'over 11'}]) }}


```


## RESULT
Condition on number : three

Condition on range : from 1 to 5


###JSON snippet

```
	"string": "Feature",
	"time": "2014-09-08T04:49:20Z",
	"date2year": "2014-01-01T04:49:20Z",
	"number": 3,
	"number_0": 0,
	"number_1": 1,
	"number_2": 2
     

```
	 
	 
	 
	 
