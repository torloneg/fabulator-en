# for

for iterates over arrays and dictionaries.

**params**

| name | type | description | allow |
| :--- | :--- | :--- | :--- |
| var | string | varible |  |
| collection | string | collection or array |  |

## example:

```text
{% for item in items %}
  <li>{{ item.title }}</li>

{% else %}
  <li>This would display if the 'item' collection were empty</li>

{% endfor %}
```

## output:

```text
list
```

