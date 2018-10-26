---
description: Description of Nunjucks
---

# Nunjucks


## abs
Return the absolute value of the argument


**params**
    |  |  |
    | :--- | :--- |


```
example: {{ -3|abs }}

output: 3
```
## capitalize
Make the first letter uppercase, the rest lower case


**params**
    |  |  |
    | :--- | :--- |


```
example: {{ "This Is A Test" | capitalize }}

output: This is a test
```
## dictsort
Sort a dict and yield (key, value) pairs


**params**
    |  |  |
    | :--- | :--- |


```
example: {% set items = {    'e': 1,
    'd': 2,
    'c': 3,
    'a': 4,
    'f': 5,
    'b': 6
} %} {% for item in items | dictsort %}    {{ item[0] }}
{% endfor %}

output: a b c d e f
```
## dump
Call JSON.stringify on an object and dump the result into the template. Useful for debugging: {{ items | dump }}.


**params**
    |  |  |
    | :--- | :--- |


```
example: {% set items = ["a", 1, { b : true}] %} {{ items | dump }}

output: a,1,[object Object]
```
## first
Get the first item in an array or the first letter if it&#x27;s a string


**params**
    |  |  |
    | :--- | :--- |


```
example: {% set items = [1,2,3] %} {{ items | first }}
{% set word = 'abc' %} {{ word | first }}

output: 1
a

```
## float
Convert a value into a floating point number. If the conversion fails 0.0 is returned. This default can be overridden by using the first parameter.


**params**
    |  |  |
    | :--- | :--- |


```
example: {{ "3.5" | float }}

output: 3.5
```
## groupby
Group a sequence of objects by a common attribute


**params**
    |  |  |
    | :--- | :--- |


```
example: {% set items = [        { name: 'james', type: 'green' },
        { name: 'john', type: 'blue' },
        { name: 'jim', type: 'blue' },
        { name: 'jessie', type: 'green' }
    ]
%}
{% for type, items in items | groupby("type") %}    <b>{{ type }}</b> :
    {% for item in items %}
        {{ item.name }}
    {% endfor %}<br>
{% endfor %}

output: green : james jessie blue : john jim

```
## int
Convert the value into an integer. If the conversion fails 0 is returned.


**params**
    |  |  |
    | :--- | :--- |


```
example: {{ "3.5" | float }}

output: 3
```
## join
Return a string which is the concatenation of the strings in a sequence


**params**
    |  |  |
    | :--- | :--- |


```
example: {% set items =  [1, 2, 3] %} {{ items | join }}
{% set items = ['foo', 'bar', 'bear'] %} {{ items | join(",") }}
{% set items = [    { name: 'foo' },
    { name: 'bar' },
    { name: 'bear' }]
%}
{{ items | join(",", "name") }}

output: 123 foo,bar,bear foo,bar,bear

```
## last
Get the last item in an array or the last letter if it&#x27;s a string:


**params**
    |  |  |
    | :--- | :--- |


```
example: {% set items = [1,2,3] %} {{ items | last }}
{% set word = 'abc' %} {{ word | last }}

output: 3
c

```
## length
Return the length of an array or string, or the number of keys in an object


**params**
    |  |  |
    | :--- | :--- |


```
example: {{ [1,2,3] | length }} {{ "test" | length }} {{ {key: value} | length }}

output: 3 4 1

```
## list
Convert the value into a list. If it was a string the returned list will be a list of characters.


**params**
    |  |  |
    | :--- | :--- |


```
example: {% for i in "foobar" | list %}{{ i }},{% endfor %}

output: f,o,o,b,a,r,

```
## upper
Convert string to all upper case


**params**
    |  |  |
    | :--- | :--- |


```
example: {{ "fOObAr" | upper }}

output: FOOBAR

```
## random
Select a random value from an array.


**params**
    |  |  |
    | :--- | :--- |


```
example: {{ [1,2,3,4,5,6,7,8,9] | random }}

output: A random value between 1-9 (inclusive).

```
## rejectattr
Filter a sequence of objects by applying a test to the specified attribute of each object, and rejecting the objects with the test succeeding.

This is the opposite of selectattr filter.

If no test is specified, the attribute’s value will be evaluated as a boolean.


**params**
    |  |  |
    | :--- | :--- |


```
example: {% set foods = [{tasty: true}, {tasty: false}, {tasty: true}]%} {{ foods | rejectattr("tasty") | length }}

output: 1
```
## replace
Replace one item with another. The first item is the item to be replaced, the second item is the replaced value.


**params**
    |  |  |
    | :--- | :--- |


```
example: {% set numbers = 123456 %} {{ numbers | replace("4", ".") }}
{% set letters = aaabbbccc%} {{ "letters" | replace("", ".") }}

output: 123.56
```
## reverse


**params**
    |  |  |
    | :--- | :--- |


```
example: {{ "abcdef" | reverse }} {% for i in [1, 2, 3, 4] | reverse %}    {{ i }}
{% endfor %}

output: fedcba
4 3 2 1

```
## round


**params**
    |  |  |
    | :--- | :--- |


```
example: {{ 4.5 | round }} {{ 4.12346 | round(4) }}

output: 5
4.1235

```
## safe
Mark the value as safe which means that in an environment with automatic escaping enabled this variable will not be escaped.

**params**
    |  |  |
    | :--- | :--- |


```
example: {{ "foo http://www.example.com/ bar" | urlize | safe }}

output: foo &lt;a href&#x3D;&quot;http://www.example.com/&quot;&gt;http://www.example.com/&lt;/a&gt; bar

```
## selectattr
Filter a sequence of objects by applying a test to the specified attribute of each object, and only selecting the objects with the test succeeding.

This is the opposite to rejectattr.

If no test is specified, the attribute’s value will be evaluated as a boolean.


**params**
    |  |  |
    | :--- | :--- |


```
example: {% set foods = [{tasty: true}, {tasty: false}, {tasty: true}]%} {{ foods | selectattr("tasty") | length }}

output: 2

```
## slice
Slice an iterator and return a list of lists containing those items:


**params**
    |  |  |
    | :--- | :--- |


```
example: {% set arr = [1,2,3,4,5,6,7,8,9] %}
<div class="columwrapper">  {%- for items in arr | slice(3) %}
    <ul class="column-{{ loop.index }}">
    {%- for item in items %}
      <li>{{ item }}</li>
    {%- endfor %}
    </ul>
  {%- endfor %}
</div>

output: &lt;div class&#x3D;&quot;columwrapper&quot;&gt;
    &lt;ul class&#x3D;&quot;column-1&quot;&gt;
      &lt;li&gt;1&lt;/li&gt;
      &lt;li&gt;2&lt;/li&gt;
      &lt;li&gt;3&lt;/li&gt;
    &lt;/ul&gt;
    &lt;ul class&#x3D;&quot;column-2&quot;&gt;
      &lt;li&gt;4&lt;/li&gt;
      &lt;li&gt;5&lt;/li&gt;
      &lt;li&gt;6&lt;/li&gt;
    &lt;/ul&gt;
    &lt;ul class&#x3D;&quot;column-3&quot;&gt;
      &lt;li&gt;7&lt;/li&gt;
      &lt;li&gt;8&lt;/li&gt;
      &lt;li&gt;9&lt;/li&gt;
    &lt;/ul&gt;
&lt;/div&gt;

```
## string
params:

**params**
    |  |  |
    | :--- | :--- |


```
example: {% set item = 1234 %} {{ item | string }}

output: &quot;1234&quot;

```
## striptags
Analog of jinja&#x27;s striptags. If preserve_linebreaks is false (default), strips SGML/XML tags and replaces adjacent whitespace with one space. If preserve_linebreaks is true, normalizes whitespace, trying to preserve original linebreaks. Use second behavior if you want to pipe {{ text | striptags(true) | escape | nl2br }}. Use default one otherwise.


**params**
    |  |  |
    | :--- | :--- |


```
example: 
output: 
```
## sum


**params**
    |  |  |
    | :--- | :--- |


```
example: {% set items = [1,2,3] %} {{ items | sum }}

output: 6

```
## title
Make the first letter of the string uppercase also a list of string


**params**
    |  |  |
    | :--- | :--- |


```
example: {{ "foo bar baz" | title }}

output: Foo Bar Baz
```
## trim


**params**
    |  |  |
    | :--- | :--- |


```
example: {{ "  foo " | trim }}

output: foo
```
## truncate
The length is specified with the first parameter which defaults to 255. If the second parameter is true the filter will cut the text at length. Otherwise it will discard the last word. If the text was in fact truncated it will append an ellipsis sign (&quot;...&quot;). A different ellipsis sign than &quot;(...)&quot; can be specified using the third parameter.
Truncate to 3 characters:


**params**
    |  |  |
    | :--- | :--- |


```
example: {{ "foo bar" | truncate(3) }} {{ "foo bar baz" | truncate(6, true, "?") }}

output: foo
foo ba ?

```
## upper
Convert the value into a list. If it was a string the returned list will be a list of characters.


**params**
    |  |  |
    | :--- | :--- |


```
example: {% for i in "foobar" | list %}{{ i }},{% endfor %}

output: f,o,o,b,a,r,

```
## urlize


**params**
    |  |  |
    | :--- | :--- |


```
example: {{ "foo http://www.example.com/ bar" | urlize | safe }}

output: foo &lt;a href&#x3D;&quot;http://www.example.com/&quot;&gt;http://www.example.com/&lt;/a&gt; bar

```
## wordcount


**params**
    |  |  |
    | :--- | :--- | 


```
example: {% set foo = "Hello World"%} {{ foo | wordcount }}

output: 2
```


