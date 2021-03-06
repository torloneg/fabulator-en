---
description: Description of String
---

# String


## String.camelize
Remove any underscores or dashes and convert a string into camel casing.


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | string  | input value received


```
example: {{ "data_rate" | String.camelize }}

output: dataRate
```
## String.capitalize
Convert all characters into uppercase letters


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | string  | input value received


```
example: {{ "foo" | String.capitalize }}

output: FOO
```
## String.chompLeft
Removes prefix from start of string.


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | string  | input value received
    | prefix | string  | string pattern


```
example: {{ "foobar" | String.chompLeft('foo') }}

output: bar
```
## String.chompRight
Removes suffix from end of string


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | string  | input value received
    | prefix | string  | string pattern


```
example: {{ "foobar" | String.chompRight('bar') }}

output: foo
```
## String.collapseWhitespace
Converts all adjacent whitespace characters to a single space.


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | string  | input value received


```
example: {{ "  String    libraries are    fun !  " | String.collapseWhitespace() }}

output: String libraries are fun !
```
## String.dasherize
Returns a converted camel cased string into a string delimited by dashes.


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | string  | input value received


```
example: {{ "dataRate" | String.dasherize() }}

output: data-rate
```
## String.decodeHTMLEntities
Decodes HTML entities into their string representation.


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | string  | input value received


```
example: {{ "Ken Thompson &amp; Dennis Ritchie" | String.decodeHTMLEntities() }}

output: Ken Thompson &amp; Dennis Ritchie
```
## String.escapeHTML
Escapes the html.


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | string  | input value received


```
example: {{ "<div>hi</div>" | String.escapeHTML() }}

output: 
```
## String.left
Return the substring denoted by n positive left-most characters.


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | string  | input value received
    | count | int  | number of char


```
example: {{ "My name is JP" | String.left(2) }}

output: My
```
## String.repeat
Returns a string repeated n times.


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | string  | input value received
    | count | int  | number of repetitions


```
example: {{ "-" | String.repeat(10) }}

output: ----------
```
## String.right
Return the substring denoted by n positive right-most characters.


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | string  | input value received
    | count | string  | number of char


```
example: {{ "My name is JP" | String.right(-2) }}

output: My
```
## String.rightReplaceChar
replace last right char


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | string  | input value received
    | char | string  | character to replace


```
example: {{ "casa" | String.rightReplaceChar("e") }}

output: case
```
## String.slugify
Converts the text into a valid url slug. Removes accents from Latin characters.


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | string  | input value received


```
example: {{ "Global Thermonuclear Warfare" | String.slugify() }}

output: global-thermonuclear-warfare
```
## String.toBoolean
Converts a a logical truth string to boolean. That is: true, 1, &#x27;true&#x27;, &#x27;on&#x27;, or &#x27;yes&#x27;.


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | string  | input value received


```
example: {{ "true" | String.toBoolean() }}

output: true
```
## String.toFloat
Return the float value, wraps parseFloat


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | string  | input value received
    | precision | int  | 


```
example: {{ 3.45522222333232 | String.toFloat(2) }}

output: 3.45
```
## String.toInt
Return the float value, wraps parseInt


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | string  | input value received
    | precision | int  | 


```
example: {{ 3.45522222333232 | String.toInt(2) }}

output: 3
```
## String.unescapeHTML
Unescapes the html.


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | string  | input value received


```
example: {{ '&lt;div&gt;hi&lt;/div&gt;' | String.unescapeHTML() }}

output: &lt;div&gt;hi&lt;/div&gt;
```
## String.wrapHTML
wrapHTML helps to avoid concatenation of element with string. the string will be wrapped with HTML Element and their attributes.


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | input | string  | input value received
    | tag | string  | html tag name


```
example: {{ 'Venkat' | String.wrapHTML('div') }}

output: &lt;div&gt;Venkat&lt;/div&gt;
```


