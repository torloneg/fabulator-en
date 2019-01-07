Examples of string filter

 
###TEMPLATE
```
* upper a string as *{{data.string}}* in **{{data.string | upper}}**

* capitalize the string *{{data.person.first_name}} {{data.person.last_name}}* as **{{data.person.first_name | String.capitalize}} {{data.person.last_name | String.capitalize}}**

* remove string **this** at left of *{{data.string_1 }}* that became **{{ data.string_1 | String.chompLeft('this')}}**

* remove string **this** from right of *{{data.string_1}}* at became **{{data.string_1 | String.chompRight('string')}}**

* replace a charcater **a** from a *{{data.string }}* that became **{{data.string | String.rightReplaceChar('a')}}**

```


###RESULT
* upper a string as Feature in FEATURE

* capitalize the string jhon smith as Jhon Smith

* remove string this at left of this is a string that became ** is a string**

* remove string this from right of this is a string at became **this is a **

* replace a charcater a from a Feature that became Featura



## CONVERT

### TEMPLATE
```
Convert string in boolean or integer

* to Boolean TRUE: {{data.string_true_1 | String.toBoolean}} / {{data.string_true_2 | String.toBoolean}}

* to Boolean FALSE : {{data.string_false_1 | String.toBoolean}} / {{data.string_false_2 | String.toBoolean}}

* to Int : {{data.string_int | String.toInt | Numeral.Add(1)}}

* to float : {{data.string_float | String.toFloat | Numeral.Add(1)}}


```

###RESULT
to Boolean TRUE: true / true

to Boolean FALSE : false / false

to Int : 2

to float : 2.1


###JSON snippet

```
	"string": "Feature",
	"string_1":"this is a string",
	"person": {
	    "first_name":"jhon",
	    "last_name":"smith"
	},	
	"string_true_1":"1",
	"string_true_2":"true",
	"string_false_1":"0",
	"string_false_2":"false",
    "string_int":"1",
	"string_float":"1.1",

```
	 
	 
	 
	 
