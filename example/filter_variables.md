# VARIABLES - FILTER

A variable looks up a value from the template context. If you wanted to simply display a variable, you would do:

## TEMPLATE

```

{% set username='fabulator'%}
**{{ username }}**

This looks up username from the context and displays it. Variable names can have dots in them which lookup properties, just like javascript. You can also use the square bracket syntax.

* {{ data.string_1 }}
* {{ data["string_1"] }}
```

## RESULT

fabulator

This looks up username from the context and displays it. Variable names can have dots in them which lookup properties, just like javascript. You can also use the square bracket syntax.

this is a string
this is a string

#### FILTERS
Filters are essentially functions that can be applied to variables. They are called with a pipe operator (|) and can take arguments.

```
* {{ data.string_1 | title }}
* {{ data.string_1 | replace("string", "**string**") | capitalize }}
```

## RESULT
This Is A String
This is a string