# TAG CONDITION

#### IF
if tests a condition and lets you selectively display content. It behaves exactly as javascript's if behaves.

## TEMPLATE

```
{% if data.string == 'Feature'  %}
  data.string == 'Feature'
{% endif %}

If variable is defined and evaluates to true, "It is true" will be displayed. Otherwise, nothing will be.

You can specify alternate conditions with elif (or elseif, which is simply an alias of elif) and else

{% if data.string == 'Feature' %}
 Ex.: data.string == 'Feature'
{% elif tired %}
 Ex.: Not Feature
{% else %}
 Ex.: Else Feature
{% endif %}

```

## RESULT

if tests a condition and lets you selectively display content. It behaves exactly as javascript's if behaves.

data.string == 'Feature'

If variable is defined and evaluates to true, "It is true" will be displayed. Otherwise, nothing will be.

You can specify alternate conditions with elif (or elseif, which is simply an alias of elif) and else

Ex.: data.string == 'Feature'

#### Comparisons

* ==
* ===
* !=
* !==
* >
* >=
* <
* <=

## TEMPLATE

```
{% if data.number !== 1 %}Number {{data.number }} IS != 1 {% endif %}
```

## RESULT

Number 3 IS != 1

#### Logic
* and
* or
* not
* Use parentheses to group expressions

## TEMPLATE
```
{% if data.number and data.number ==3 %}data.number exist and data.number == 3{% endif %}
```
## RESULT
data.number exist and data.number == 3





