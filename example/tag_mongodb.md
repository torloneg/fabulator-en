# TAG MONGODB

Example of search on mongodb

#### **MongoDB query** 
method queries a collection by setting a query in the MongoDB format.
Search all cities in the region abruzzo in italy

## TEMPLATE

```
{% set query_mongodb = "{ \"district\": \"abruzzo\" }" %}

{% DB_MongoQuery url=$DATABASE_MONGODB,collection="Meteo_History",query=query_mongodb,skip=0,limit=10,sort="{}",select="{}",context="items" %}
{% for item in items %}
* {{ item.city | title }} : MIN ( {{item.temperatures.min.value }}°C ) MAX ( {{item.temperatures.max.value }}°C )
{% endfor %}
{% error %}

{% END_DB_MongoQuery %}

```

## RESULT

* Chieti : MIN ( 6°C ) MAX ( 16°C )
* L'aquila : MIN ( 3°C ) MAX ( 12°C )
* Pescara : MIN ( 7°C ) MAX ( 18°C )
* Teramo : MIN ( 5°C ) MAX ( 12°C )

#### **MongoDB geospatial query**
It is possible to make geospatial queries on data stored on a MongoDB. In this case the earthquakes are searched by setting the position in longitude and latitude

```
{"$and":[{"loc":{"$near":{"$geometry":{"type":"Point","coordinates":[13.3157262,42.3633634]},"$minDistance":0,"$maxDistance":100000}}},{"magnitude":{"$gte":5}}]}
```
    
## TEMPLATE

```
{% DB_MongoNear url=$DATABASE_MONGODB,collection="Quake_History", latitude=data.geometry.coordinates.latitude, longitude=data.geometry.coordinates.longitude , query="{\"magnitude\": { \"$gte\": 5.0 } }",skip=0,limit=10,sort="{\"time\": 1}",select="{}",context="items" %}
{% text %}
 
 
{% endtext %}
the result obtained

{% for item in items %}
{% text %}* {{ item.description | title }} - magnitudo {{ item.magnitude }} Richter - {{ item.time | Moment.Add(2,'h','DD/MM/YYYY hh:mm:ss') }}{% endtext %}
{% endfor %}
{% error %}

{% End_DB_MongoNear %}
```

## RESULT

* 2 Km Sw L'aquila (aq) - magnitudo 6.1 Richter - 06/04/2009 03:32:40

* 8 Km E Pizzoli (aq) - magnitudo 5 Richter - 07/04/2009 01:15:36

* 1 Km N Fossa (aq) - magnitudo 5.4 Richter - 07/04/2009 07:47:37

* 5 Km Se Capitignano (aq) - magnitudo 5.2 Richter - 09/04/2009 02:52:59

* 4 Km E Capitignano (aq) - magnitudo 5 Richter - 09/04/2009 09:38:16
