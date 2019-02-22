
# TAG macro

macro allows you to define reusable chunks of content. It is similar to a function in a programming language.


**params**
    | name | type  | description | allow
    | :--- | :---  | :---        | :---       |



### example:
```
{% macro field(name, value='', type='text') %} type: {{ type }}
{% endmacro %}

```

### output:
```
type: text

```


