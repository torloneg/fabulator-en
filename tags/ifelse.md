# ifelse

if tests a condition and lets you selectively display content. It behaves exactly as javascript's if behaves.

**params**

| name | type | description | allow |
| :--- | :--- | :--- | :--- |


## example:

```text
{% if variable %} It is true{% endif %}
{% if hungry %}  I am hungry
{% elif tired %}  I am tired
{% else %}  I am good!
{% endif %}
```

## output:

```text
It is true
```

