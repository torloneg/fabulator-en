
# TAG DB_MongoQuery

query a MongoDB collection


**params**
    | name | type  | description |
    | :--- | :---  | :---        |
    | url | string  | connection string  |
    | collection | string  | collection name  |
    | query | string  | query in mngodb format or a variable name with the query  |
    | skip | number  | first record  |
    | limit | number  | number of record  |
    | select | string  | string with field list  |
    | sort | string  | field to sort the result  |
    | context | string  | new variable to insert the result in json format  |



### example:
```{% set query_mongodb = "{ \"district\": \"abruzzo\" }" %}
{% DB_MongoQuery url=$DATABASE_MONGODB,collection="Meteo_History",query=query_mongodb,skip=0,limit=10,sort="{}",select="{}",context="items" %} {% for item in items %} * {{ item.city | title }} : MIN ( {{item.temperatures.min.value }}°C ) MAX ( {{item.temperatures.max.value }}°C ) {% endfor %} {% error %}
{% END_DB_MongoQuery %}
```

### output:
```Chieti : MIN ( 6°C ) MAX ( 16°C )
L&#x27;aquila : MIN ( 3°C ) MAX ( 12°C )
Pescara : MIN ( 7°C ) MAX ( 18°C )
Teramo : MIN ( 5°C ) MAX ( 12°C )
```


