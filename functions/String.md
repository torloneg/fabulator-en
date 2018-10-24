---
description: Description of String
---

# String


## String.camelize
Remove any underscores or dashes and convert a string into camel casing.

{% hint style="info" %}
*params*
{% endhint %}

```
example: {{ "data_rate" | String.camelize }}

output: dataRate
```
## String.capitalize
Convert all characters into uppercase letters

{% hint style="info" %}
*params*
{% endhint %}

```
example: {{ "foo" | String.capitalize }}

output: FOO
```
## String.chompLeft
Removes prefix from start of string.

{% hint style="info" %}
*params*
    | title | part of string  |
    | type | string |
    | value |  |
{% endhint %}

```
example: {{ "foobar" | String.foobar('foo') }}

output: bar
```
## String.chompRight
Removes suffix from end of string

{% hint style="info" %}
*params*
    | title | part of string  |
    | type | string |
    | value |  |
{% endhint %}

```
example: {{ "foobar" | String.chompRight('bar') }}

output: foo
```
## String.collapseWhitespace
Converts all adjacent whitespace characters to a single space.

{% hint style="info" %}
*params*
{% endhint %}

```
example: {{ "  String    libraries are    fun !  " | String.collapseWhitespace() }}

output: String libraries are fun !
```
## String.dasherize
Returns a converted camel cased string into a string delimited by dashes.

{% hint style="info" %}
*params*
{% endhint %}

```
example: {{ "dataRate" | String.dasherize() }}

output: data-rate
```
## String.decodeHTMLEntities
Decodes HTML entities into their string representation.

{% hint style="info" %}
*params*
{% endhint %}

```
example: {{ "Ken Thompson &amp; Dennis Ritchie" | String.decodeHTMLEntities() }}

output: Ken Thompson &amp; Dennis Ritchie
```
## String.escapeHTML
Escapes the html.

{% hint style="info" %}
*params*
{% endhint %}

```
example: {{ "<div>hi</div>" | String.escapeHTML() }}

output: 
```
## String.left
Return the substring denoted by n positive left-most characters.

{% hint style="info" %}
*params*
    | title | index  |
    | type | int |
    | value |  |
{% endhint %}

```
example: {{ "My name is JP" | String.left(2) }}

output: My
```
## String.repeat
Returns a string repeated n times.

{% hint style="info" %}
*params*
    | title | number of repeater  |
    | type | int |
    | value |  |
{% endhint %}

```
example: {{ "-" | String.repeat(10) }}

output: ----------
```
## String.right
Return the substring denoted by n positive right-most characters.

{% hint style="info" %}
*params*
    | title | index position  |
    | type | int |
    | value |  |
{% endhint %}

```
example: {{ "My name is JP" | String.right(-2) }}

output: My
```
## String.rightReplaceChar
replace last right char

{% hint style="info" %}
*params*
    | title | new char to replace  |
    | type | int |
    | value |  |
{% endhint %}

```
example: {{ "casa" | String.rightReplaceChar("e") }}

output: case
```
## String.slugify
Converts the text into a valid url slug. Removes accents from Latin characters.

{% hint style="info" %}
*params*
{% endhint %}

```
example: {{ "Global Thermonuclear Warfare" | String.slugify() }}

output: global-thermonuclear-warfare
```
## String.toBoolean
Converts a a logical truth string to boolean. That is: true, 1, &#x27;true&#x27;, &#x27;on&#x27;, or &#x27;yes&#x27;.

{% hint style="info" %}
*params*
{% endhint %}

```
example: {{ "true" | String.toBoolean() }}

output: true
```
## String.toFloat
Return the float value, wraps parseFloat

{% hint style="info" %}
*params*
    | title | precision  |
    | type | int |
    | value |  |
{% endhint %}

```
example: {{ 3.45522222333232 | String.toFloat(2) }}

output: 3.45
```
## String.toInt
Return the float value, wraps parseInt

{% hint style="info" %}
*params*
    | title | precision  |
    | type | int |
    | value |  |
{% endhint %}

```
example: {{ 3.45522222333232 | String.toInt(2) }}

output: 3
```
## String.unescapeHTML
type: filter
group: string
origin: custom
description: |
       Unescapes the html.
params:
return: string
input: &gt;
        {{ &#x27;&amp;lt;div&amp;gt;hi&amp;lt;/div&amp;gt;&#x27; | String.unescapeHTML() }}
output: &lt;div&gt;hi&lt;/div&gt;

{% hint style="info" %}
*params*
{% endhint %}

```
example: 
output: 
```
## String.wrapHTML
wrapHTML helps to avoid concatenation of element with string. the string will be wrapped with HTML Element and their attributes.

{% hint style="info" %}
*params*
{% endhint %}

```
example: {{ 'Venkat' | String.wrapHTML('div') }}

output: &lt;div&gt;Venkat&lt;/div&gt;
```


