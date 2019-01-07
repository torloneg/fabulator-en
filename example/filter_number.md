
Examples of transformation of numbers into natural language

## ITALIAN

### TEMPLATE
```
the number **1** is transformed into Italian language **{{ 1 | Numeral.OrdinalToLanguage('it') }}** or **{{ 1 | Numeral.OrdinalToLanguage('it') | String.rightReplaceChar("a")}}**

the number **{{data.number}}** is transformed into Italian language **{{data.number | Numeral.NumberToLanguage('it')}}**

the number **{{data.double}}** is transformed into Italian language **{{data.double | Numeral.NumberToLanguage('it')}}**

the number **{{data.accounting.money_3}}** is transformed into Italian language **{{data.accounting.money_3 | Numeral.NumberToLanguage('it')}}**


numbers with positive or negative sign can be used to describe situations in natural language: 
* {{data.sign.positive}} is {{data.sign.positive| Numeral.Sign('positivo','negativo','parità')}}
* {{data.sign.negative}} is {{data.sign.negative| Numeral.Sign('positivo','negativo','parità')}}
* {{data.sign.parity}} is {{data.sign.parity| Numeral.Sign('positivo','negativo','parità')}}

Pluralize: {{data.number | Numeral.Pluralize('singolare','plurale','nullo')}}

 
```


### RESULT
the number 1 is transformed into Italian language primo or prima

the number 3 is transformed into Italian language tre

the number 2.1 is transformed into Italian language due e uno

the number 4999.99 is transformed into Italian language quattromilanovecentonovantanove e novantanove

numbers with positive or negative sign can be used to describe situations in natural language:

* 1 is positivo
* -1 is negativo
* 0 is parità
* Pluralize: plurale

## ENGLISH
### TEMPLATE
```
NumberToLanguage **(EN)**: **{{data.number}}** is **{{data.number | Numeral.NumberToLanguage('en')}}**, **{{data.number_0}}** is **{{data.number_0 | Numeral.NumberToLanguage('en')}}**

* {{data.sign.positive}} is {{data.sign.positive| Numeral.Sign('positive','negative','parity')}}
* {{data.sign.negative}} is {{data.sign.negative| Numeral.Sign('positive','negative','parity')}}
* {{data.sign.parity}} is {{data.sign.parity| Numeral.Sign('positive','negative','parity')}}



Pluralize: {{ data.number_2 }} is is  {{data.number_2 | Numeral.Pluralize('singular','plural','null')}}

Pluralize: {{ data.number_1 }} is {{ data.number_1 | Numeral.Pluralize('singular','plural','null')}}

```

### RESULT
NumberToLanguage (EN): 3 is three, 0 is zero

* 1 is positive
* -1 is negative
* 0 is parity

* Pluralize: 2 is is plural
* Pluralize: 1 is singular


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
	 
	 
	 
	 
