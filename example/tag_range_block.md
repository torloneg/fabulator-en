There are tags to use to write portions of text if the value is within a range (min/mx) or outside these limits
 
### TEMPLATE

```
  
Internal value at min - max range
  {% set valueIn = 5 %}
  
  Example if **{{valueIn}}** is btween 1 and 6 show a text :
 {% inRangeBlock value=valueIn,min=1,max=6 %}
   *Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque vestibulum id dui non venenatis. Integer sit amet maximus velit. Morbi quis egestas lectus, feugiat aliquam ex.*
 {% else %}
    Vivamus ultrices sem ut orci semper, sed convallis ex suscipit. 
 {% endinRangeBlock %}

external value at min - max range

 {% outRangeBlock value=valueIn,min=1,max=6 %}
   *Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque vestibulum id dui non venenatis. Integer sit amet maximus velit. Morbi quis egestas lectus, feugiat aliquam ex.*
 {% else %}
  *Vivamus ultrices sem ut orci semper, sed convallis ex suscipit.*
 {% endoutRangeBlock %}

```

### RESULT

There are tags to use to write portions of text if the value is within a range (min/mx) or outside these limits

Internal value at min - max range

Example if 5 is btween 1 and 6 show a text :

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque vestibulum id dui non venenatis. Integer sit amet maximus velit. Morbi quis egestas lectus, feugiat aliquam ex.

external value at min - max range

Vivamus ultrices sem ut orci semper, sed convallis ex suscipit.
