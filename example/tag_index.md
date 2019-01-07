# INDEX

Returns a json object indicating a specific location in the collection or the "last" and "first" strings.

## TEMPLATE

```text
![Showdown][sd-logo]

returns a json object indicating a specific location in the collection or the "last" and "first" strings

Collection :

 {{ data.collection | dump }}

 output :

 **pos = 3**
 {% set pos = 3 %}
 {% index value=data.collection,index=pos %}
  {{index | dump }}
 {% endindex %}

  **pos = 1**
 {% set pos = 1 %}
 {% index value=data.collection,index=pos %}
  {{index | dump }}
 {% endindex %}

   **pos = "last"**
 {% set pos = "last" %}
 {% index value=data.collection,index=pos %}
  {{index | dump }}
 {% endindex %}
```

## RESULT

returns a json object indicating a specific location in the collection or the "last" and "first" strings

Collection :

\[{"itemid":"1092","description":"ELEMENT \#1","date":"2017-08-09"},{"itemid":"2192","description":"ELEMENT \#2","date":"2017-07-08"},{"item\_id":"2193","description":"ELEMENT \#3","date":"2018-07-08"}\]

output :

pos = 3

{"item\_id":"2193","description":"ELEMENT \#3","date":"2018-07-08"}

pos = 1

{"item\_id":"1092","description":"ELEMENT \#1","date":"2017-08-09"}

pos = "last"

{"item\_id":"2193","description":"ELEMENT \#3","date":"2018-07-08"}

