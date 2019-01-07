for iterates over arrays and dictionaries.

### TEMPLATE

```
Elements taken from an array or collection

 {% for item in data.collection %}
  <li>{{ item.description }}</li>
{% else %}
  <li>This would display if the 'item' collection were empty</li>
{% endfor %}

when array is empty

 {% for item in items %}
  <li>{{ item.title }}</li>
{% else %}
  <li>This would display if the 'item' collection were empty</li>
{% endfor %}

Inside loops, you have access to a few special variables:

* **loop.index**: the current iteration of the loop (1 indexed)
* **loop.index0**: the current iteration of the loop (0 indexed)
* **loop.revindex**: number of iterations until the end (1 indexed)
* **loop.revindex0**: number of iterations until the end (0 based)
* **loop.first**: boolean indicating the first iteration
* **loop.last**: boolean indicating the last iteration
* **loop.length**: total number of items

```

### RESULT

Elements taken from an array or collection

ELEMENT #1
ELEMENT #2
ELEMENT #3
when array is empty

This would display if the 'item' collection were empty
Inside loops, you have access to a few special variables:

* **loop.index**: the current iteration of the loop (1 indexed)
* **loop.index0**: the current iteration of the loop (0 indexed)
* **loop.revindex**: number of iterations until the end (1 indexed)
* **loop.revindex0**: number of iterations until the end (0 based)
* **loop.first**: boolean indicating the first iteration
* **loop.last**: boolean indicating the last iteration
* **loop.length**: total number of items