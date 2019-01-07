## MACRO
macro allows you to define reusable chunks of content. It is similar to a function in a programming language.  

### TEMPLATE

```
{% macro Debug(p) %}

Show json content : {{ p | dump }}

{% endmacro %}
 
{% macro MrMs(p) %}
{% text clear="cr,lf" %}
{% if p.sex =='M' %}**Mr.** {% endif %}
{% if p.sex =='F' %}**Ms.** {% endif %}
{{p.first_name | title}} {{p.last_name | title}}
{% endtext %}
{% endmacro %}

Simple macro for debug :
{{ Debug(data.person) }}


Example:

{{ MrMs(data.person_m)}}
{{ MrMs(data.person_f)}}


```

### RESULT
Simple macro for debug :

Show json content : {"firstname":"jhon","lastname":"smith","sex":"M"}

Example:

Mr. Jhon Smith

Ms. Rose Smith

--

## FILTER
A filter block allows you to call a filter with the contents of the block. Instead passing a value with the | syntax, the render contents from the block will be passed.

### TEMPLATE

```
applies the **title** function to the contents of the block

* may the force be with you -> {% filter title %}
may the force be with you
{% endfilter %}

applies the **replace** function to the contents of the block
* may the force be with you -> {% filter replace("force", "forth") %}
may the force be with you
{% endfilter %}
```

### RESULT

applies the title function to the contents of the block

may the force be with you -> may The Force Be With You
applies the replace function to the contents of the block

may the force be with you -> may the forth be with you