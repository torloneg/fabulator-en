
# TAG InRangeBlock

shows the text in the main block if the value is within the range min,max


**params**
    | name | type  | description | allow
    | :--- | :---  | :---        | :---       |
    | min | number  | min value of range  | 
    | max | number  | max value of range  | 



### example:
```
{% set valueIn = 5 %}
{% inRangeBlock value=valueIn,min=1,max=6 %}
  BLOCK

{% else %}
  BLOCK ELSE

{% endinRangeBlock %}

```

### output:
```
BLOCK

```


