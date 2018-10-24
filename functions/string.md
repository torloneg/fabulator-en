---
description: Description of String
---

# String

## String.camelize

Remove any underscores or dashes and convert a string into camel casing.

_params_

```text
example: {{ "data_rate" | String.camelize }}

output: dataRate
```

## String.capitalize

Convert all characters into uppercase letters

_params_

```text
example: {{ "foo" | String.capitalize }}

output: FOO
```

## String.chompLeft

Removes prefix from start of string.

_params_ \| title \| part of string \| \| type \| string \| \| value \| \|

```text
example: {{ "foobar" | String.foobar('foo') }}

output: bar
```

## String.chompRight

Removes suffix from end of string

_params_ \| title \| part of string \| \| type \| string \| \| value \| \|

```text
example: {{ "foobar" | String.chompRight('bar') }}

output: foo
```

## String.collapseWhitespace

Converts all adjacent whitespace characters to a single space.

_params_

```text
example: {{ "  String    libraries are    fun !  " | String.collapseWhitespace() }}

output: String libraries are fun !
```

## String.dasherize

Returns a converted camel cased string into a string delimited by dashes.

_params_

```text
example: {{ "dataRate" | String.dasherize() }}

output: data-rate
```

## String.decodeHTMLEntities

Decodes HTML entities into their string representation.

_params_

```text
example: {{ "Ken Thompson &amp; Dennis Ritchie" | String.decodeHTMLEntities() }}

output: Ken Thompson &amp; Dennis Ritchie
```

## String.escapeHTML

Escapes the html.

_params_

```text
example: {{ "<div>hi</div>" | String.escapeHTML() }}

output:
```

## String.left

Return the substring denoted by n positive left-most characters.

_params_ \| title \| index \| \| type \| int \| \| value \| \|

```text
example: {{ "My name is JP" | String.left(2) }}

output: My
```

## String.repeat

Returns a string repeated n times.

_params_ \| title \| number of repeater \| \| type \| int \| \| value \| \|

```text
example: {{ "-" | String.repeat(10) }}

output: ----------
```

## String.right

Return the substring denoted by n positive right-most characters.

_params_ \| title \| index position \| \| type \| int \| \| value \| \|

```text
example: {{ "My name is JP" | String.right(-2) }}

output: My
```

## String.rightReplaceChar

replace last right char

_params_ \| title \| new char to replace \| \| type \| int \| \| value \| \|

```text
example: {{ "casa" | String.rightReplaceChar("e") }}

output: case
```

## String.slugify

Converts the text into a valid url slug. Removes accents from Latin characters.

_params_

```text
example: {{ "Global Thermonuclear Warfare" | String.slugify() }}

output: global-thermonuclear-warfare
```

## String.toBoolean

Converts a a logical truth string to boolean. That is: true, 1, 'true', 'on', or 'yes'.

_params_

```text
example: {{ "true" | String.toBoolean() }}

output: true
```

## String.toFloat

Return the float value, wraps parseFloat

_params_ \| title \| precision \| \| type \| int \| \| value \| \|

```text
example: {{ 3.45522222333232 | String.toFloat(2) }}

output: 3.45
```

## String.toInt

Return the float value, wraps parseInt

_params_ \| title \| precision \| \| type \| int \| \| value \| \|

```text
example: {{ 3.45522222333232 | String.toInt(2) }}

output: 3
```

## String.unescapeHTML

type: filter group: string origin: custom description: \| Unescapes the html. params: return: string input: &gt;  output: &lt;div&gt;hi&lt;/div&gt;

_params_

```text
example: 
output:
```

## String.wrapHTML

wrapHTML helps to avoid concatenation of element with string. the string will be wrapped with HTML Element and their attributes.

_params_

```text
example: {{ 'Venkat' | String.wrapHTML('div') }}

output: &lt;div&gt;Venkat&lt;/div&gt;
```

