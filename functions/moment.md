---
description: Description of Moment
---

# Moment


## Moment.Add
adds any time entity to the date


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | string  | input value received
    | int | string  | number of unit to add
    | what | string  | d for day, m for month, y for year
    | format | string  | date format


```
example: {{"31/10/2018" |Moment.Add(1,"d","DD/MM/YYYY")}}

output: 1/11/2018

```
## Moment.AgeDays
numbers of days elapsed between the input date and today


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | string  | input value received


```
example: {{"31/10/2018" |Moment.AgeDays()}}

output: 30

```
## Moment.AgeYear
numbers of years elapsed between the input date and today


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | string  | input value received


```
example: {{"31/10/2000" |Moment.AgeYear()}}
{{"31/10/2017" |Moment.AgeYear()}}

output: 18
1

```
## Moment.Date
date in extended format in the passed language as a parameter


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | string  | input value received
    | language | string  | *en* for english or *it* for italian


```
example: {{"31/10/2018" | Moment.Date("en")}}
 {{"30/10/2018" |Moment.Date("it")}}

output: 
31 november 2018

31 novembre 2018

```
## Moment.DateTime
date in extended format in the passed language as a parameter


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | string  | input value received
    | language | string  | *en* for english or *it* for italian


```
example: {{"25/12/2018 12:30" | Moment.DateTime("it")}}
{{"25/12/2018 12:30" |Moment.DateTime("en")}}

output: 31 november 2018 alle ore 12 e 30

31 novembre 2018 12:30

```
## Moment.Format
Returns a date in compact format


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | string  | input value received
    | language | string  | *en* for english or *it* for italian
    | format | string  | date format


```
example: {{"31/10/2018" | Moment.Format("en","DD MMM YYYY")}}

output: 31 november 2018

```
## Moment.FromNow
returns the day in the language indicated as parameter


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | string  | input value received
    | language | string  | *en* for english or *it* for italian


```
example: {{"31/10/2018" | Moment.FromNow("en")}}
{{"30/10/2018" |Moment.AgeYear("it")}}

output: today

yesterday

```
## Moment.MonthOfYear
returns the month in letters in the language indicated as a parameter


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | string  | input value received
    | language | string  | *en* for english or *it* for italian


```
example: {{"31/10/2018" | Moment.MonthOfYear("en")}}
{{"30/10/2018" |Moment.AgeYear("it")}}

output: november

novembre

```
## Moment.Now
Now in format string


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | string  | input value received
    | language | string  | *en* for english or *it* for italian
    | format | string  | date format


```
example: {{"" |Moment.Now('it','DD/MM/YYYY hh:mm:ss')}}
{{"" |Moment.Now('it','DD MMM YYYY')}}

output: 31/10/2018 22:22:22

31 Ottobre 2018

```
## Moment.DateTime
date in extended format in the passed language as a parameter


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | string  | input value received
    | language | string  | *en* for english or *it* for italian


```
example: {{"25/12/2018 12:30" | Moment.DateTime("it")}}
{{"25/12/2018 12:30" |Moment.DateTime("en")}}

output: 12 e 30

12:30

```
## Moment.timeWithTimezone
Returns the date in the indicated timezone


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | string  | input value received
    | language | string  | 
    | format | string  | 


```
example: {{"25/12/2018 12:30" | Moment.timeWithTimezone("it","DD/MM/YYYY ")}}
{{"25/12/2018 12:30" | Moment.timeWithTimezone("it","DD/MM/YYYY ")}}

output: 

```


