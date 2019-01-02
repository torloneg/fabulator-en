
# TAG for

for iterates over arrays and dictionaries.


**params**
    | name | type  | description | allow
    | :--- | :---  | :---        | :---       |
    | var | editor  |   | 
    | in | string  |   | 
    | list | editor  |   | 



### example:
```
{% for item in items %}  <li>{{ item.title }}</li>
{% else %}  <li>This would display if the 'item' collection were empty</li>
{% endfor %}

```

### output:
```
list
```


