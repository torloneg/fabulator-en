
# TAG DB_MongoNear

executes a geolocated query on a MongoDB collection


**params**
    | name | type  | description |
    | :--- | :---  | :---        |
    | url | string  | connection string  |
    | collection | string  | collection name  |
    | query | string  | query in mongodb format with GEO condition or a variable name with the query  |
    | latitude | double  | center latitude  |
    | longitude | double  | center longitude  |
    | minDistance | number  | min distance in meter from center  |
    | maxDistance | number  | max distance in meter from center  |
    | skip | number  | first record  |
    | limit | number  | number of record  |
    | select | string  | string with field list  |
    | sort | string  | field to sort the result  |
    | context | string  | new variable to insert the result in json format  |



### example:
```
{% DB_MongoNear url=$DATABASE_MONGODB,collection="Quake_History", latitude=data.geometry.coordinates.latitude, longitude=data.geometry.coordinates.longitude , query="{\"magnitude\": { \"$gte\": 5.0 } }",skip=0,limit=10,sort="{\"time\": 1}",select="{}",context="items" %}
{% for item in items %}
{% text %}* {{ item.description | title }} - magnitudo {{ item.magnitude }} Richter - {{ item.time | Moment.Add(2,'h','DD/MM/YYYY hh:mm:ss') }}
{% endfor %}
{% error %}
{% End_DB_MongoNear %}

```

### output:
```
2 Km Sw L'aquila (aq) - magnitudo 6.1 Richter - 06/04/2009 03:32:40
8 Km E Pizzoli (aq) - magnitudo 5 Richter - 07/04/2009 01:15:36
1 Km N Fossa (aq) - magnitudo 5.4 Richter - 07/04/2009 07:47:37
5 Km Se Capitignano (aq) - magnitudo 5.2 Richter - 09/04/2009 02:52:59
4 Km E Capitignano (aq) - magnitudo 5 Richter - 09/04/2009 09:38:16

```


