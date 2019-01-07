
Several functions have been realized to obtain information in natural language starting from the dates present in the json

 
### TEMPLATE
```
* It's been {{data.time | Moment.AgeYear}} years since the  {{data.time | Moment.Format('it','YYYY')}}
* It's been {{data.time | Moment.AgeDays}} days from {{data.time | Moment.Format('en','LL')}}

The functions allow you to indicate the format to be used for the display a date
* DateFormat it/LL: {{data.time | Moment.Format('it','LL')}}
* DateFormat en/LL: {{data.time | Moment.Format('en','LL')}}

It is possible to extract day, month and year from the date in the indicated language
* E' il mese di **{{$NOW | Moment.MonthOfYear('it') | title}}**
* It is the month of **{{$NOW | Moment.MonthOfYear('en')}}**

You can specify a timezone or use the server default

* DateTime Timezone {{ $TIMEZONE }} : {{data.time|Moment.timeWithTimezone( $TIMEZONE,'HH')}}

A global variable with the date and time of the server is available

* The server time is  **{{ $NOW | Moment.DateTime('en')}}** in english and **{{ $NOW | Moment.DateTime('it')}}** in italian

* Time it: {{$NOW| Moment.Time('it')}}
* Time en: {{$NOW | Moment.Time('en')}}

```


### RESULT
* It's been 4 years since the 2014
* It's been 1582 days from September 8, 2014

The functions allow you to indicate the format to be used for the display a date

* DateFormat it/LL: 8 settembre 2014
* DateFormat en/LL: September 8, 2014

It is possible to extract day, month and year from the date in the indicated language

* E' il mese di Gennaio
* It is the month of January

You can specify a timezone or use the server default

* DateTime Timezone Europe/Rome : 06
* A global variable with the date and time of the server is available

The server time is 7 January 2019 12:18 in english and 7 gennaio 2019 alle ore 12 e 18 in italian
* Time it: 12 e 18
* Time en: 12:18 



###JSON snippet

```
{
"string": "Feature",
"time": "2014-09-08T04:49:20Z",
"date2year": "2014-01-01T04:49:20Z"
}

```
	 
	 
	 
	 
