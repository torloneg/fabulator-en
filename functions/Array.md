---
description: Description of Array
---

# Array


## Array.allValuesSame
returns true if all elements in the list are equal


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | value | array  | 
    | value | object  | 


```
example: {{  [0,0,0,0]  | Array.allValuesSame(0)}} {{  [true,false,true,true]  | Array.allValuesSame(true)}}

output: true
false

```
## Array.Contains
Returns true if any of the values in the list pass the predicate truth test


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | value | array  | array list of element in input
    | predicate | object  | predicate to test


```
example: {{  [0,0,0,0]  | Array.Contains(0)}} {{  [1, 2, 3]  | Array.Contains(3)}}

output: true
true

```
## Array.Every
Returns true if all of the values in the list pass the predicate truth test. Short-circuits and stops traversing the list if a false element is found. predicate is transformed through iteratee to facilitate shorthand syntaxes.


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | value | array  | array list of element in input
    | predicate | object  | predicate truth test


```
example: {{  [0,0,0,0]  | Array.Every(0)}} {{  [true,false,true,true]  | Array.Every(true)}}

output: true
false

```
## Array.Filter
Looks through each value in the list, returning an array of all the values that pass a truth test


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | value | array  | array list of element in input
    | filter | object  | 


```
example: {{  [1,2,3,4,5]  | Array.Filter(2)}}

output: [2 ]

```
## Array.First
First element from array


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | value | array  | 


```
example: {{  [{name: 'moe', age: 40}, {name: 'larry', age: 50}, {name: 'curly', age: 60}]  | Array.Last()}}

output: {name: &#x27;moe&#x27;, age: 40}

```
## Array.Index
Get a object by index


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | value | array  | 
    | index | number  | 


```
example: {{  [{name: 'moe', age: 40}, {name: 'larry', age: 50}, {name: 'curly', age: 60}]  | Array.Index(0)}}

output: {name: &#x27;moe&#x27;, age: 40}

```
## Array.Initial
Initial element from array


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | value | array  | 
    | count | number  | 


```
example: {{  [{name: 'moe', age: 40}, {name: 'larry', age: 50}, {name: 'curly', age: 60}]  | Array.Initial(2)}}

output: [{name: &#x27;moe&#x27;, age: 40}, {name: &#x27;larry&#x27;, age: 50} ]

```
## Array.Last
Last element from array


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | value | array  | 


```
example: {{  [{name: 'moe', age: 40}, {name: 'larry', age: 50}, {name: 'curly', age: 60}]  | Array.Last()}}

output: {name: &#x27;curly&#x27;, age: 60}

```
## Array.Lookup
uses the input value as a search key in the collection passed as an argument. If there are no values that meet the condition is returned the string passed as


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | value | string  | 
    | array | array  | 


```
example: {{  "Striker"  | Array.Lookup([{value:"Striker",text:"l'attaccante"},{value:"defender",text:"il difensore"},{value:"midfielder",text:"il centrocampista"}],"")}}

output: l&#x27;attaccante

```
## Array.Pluck
extracting a list of property values.


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | value | array  | 
    | name | string  | 


```
example: {{  [{name: 'moe', age: 40}, {name: 'larry', age: 50}, {name: 'curly', age: 60}]  | Array.Pluck('name')}}

output: [&quot;moe&quot;, &quot;larry&quot;, &quot;curly&quot;]

```
## Array.Rest
Returns the rest of the elements in an array. Pass an index to return the values of the array from that index onward.


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | value | array  | 
    | index | number  | 


```
example: {{  [{name: 'moe', age: 40}, {name: 'larry', age: 50}, {name: 'curly', age: 60}]  | Array.Rest(1)}}

output: [{name: &#x27;curly&#x27;, age: 60}]

```
## Array.Some
Returns true if any of the values in the list pass the predicate truth test


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | value | array  | 
    | predicate | Number|String|Boolean  | 


```
example: {{  [0,0,0,0]  | Array.Some(0)}} {{  [true,false,true,true]  | Array.Some(true)}}

output: true
true

```
## Array.ValueByIndex
use value as index of array


**params**
    | name | type  | description
    | :--- | :---  | :---        |
    | value | Number  | 
    | List | Array  | 


```
example: {{  1 | Array.ValueByIndex([{name: 'moe', age: 40}, {name: 'larry', age: 50}, {name: 'curly', age: 60}] )}}

output: {name: &#x27;larry&#x27;, age: 50}

```


