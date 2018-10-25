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
## title
Make the first letter of the string uppercase also a list of string


**params**
    |  |  |
    | :--- | :--- |


```
example: {{ "foo bar baz" | title }}

output: Foo Bar Baz
```


