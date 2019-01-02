
# TAG OutRangeBlock

shows the text in the main block if the value is external in the range min,max


**params**
    | name | type  | description | allow
    | :--- | :---  | :---        | :---       |
    | min | number  | min value of range  | 
    | max | number  | max value of range  | 



### example:
```
{% set valueIn = 5 %}
{% outRangeBlock value=valueIn,min=1,max=6 %}
  BLOCK

{% else %}  ELSE BLOCK
{% endoutRangeBlock %}

```

### output:
```
ELSE BLOCK

```


