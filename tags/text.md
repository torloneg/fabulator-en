
# TAG text

block to handle a text within another tag


**params**
    | name | type  | description | allow
    | :--- | :---  | :---        | :---       |
    | clear | string  | block to delimit the text  | cr,lf



### example:
```
{% text clear="cr,lf" %}
Risultato di parità con {{data.score1}} ...
{% endtext %}

```

### output:
```
Risultato di parità con 4 ...

```


