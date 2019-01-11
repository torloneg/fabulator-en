Fabulator API
=============
Endpoint Example

**Version:** 1.0.0


### Security
---
**bearer**  

|apiKey|*API Key*|
|---|---|
|Name|Authorization|
|In|header|

**<TOKEN>** value returned by the authentication function

### /example/v1/info/{iddomain}/{id}
---
##### ***GET***
**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| iddomain | path |  | Yes | string |
| id | path |  | Yes | string |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| default | Successful | string |

```
curl -X GET --header 'Accept: application/json' --header 'Authorization: <TOKEN>' 'https://api.fabulator.io/example/v1/info/**<iddomain>**/**<id>**'
```

### /example/v1/add/{iddomain}
---
##### ***POST***
**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| iddomain | path |  | Yes | string |
| body | body |  | No | [Model 4](#model-4) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| default | Successful | string |

```
curl -X POST --header 'Content-Type: application/json' --header 'Accept: application/json' --header 'Authorization: <TOKEN>' -d '{
  "name": "string",
  "description": "string",
  "json": {}
}' 'https://api.fabulator.io/example/v1/add/11111111111111'
```

### /example/v1/query/{iddomain}/{skip}/{limit}
---
##### ***POST***
**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| iddomain | path |  | Yes | string |
| skip | path |  | Yes | number |
| limit | path |  | Yes | number |
| body | body |  | No | [Model 9](#model-9) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| default | Successful | string |

```
curl -X POST --header 'Content-Type: application/json' --header 'Accept: application/json' --header 'Authorization: <TOKEN>' -d '{
  "select": "{}",
  "order": {
    "field": "date_update",
    "dir": 1
  },
  "query": "{}"
}' 'https://api.fabulator.io/example/v1/query/111111111/0/30'
```


## /example/v1/{iddomain}/{id}
---
##### ***DELETE***
**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| iddomain | path |  | Yes | string |
| id | path |  | Yes | string |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| default | Successful | string |

```
curl -X PUT --header 'Content-Type: application/json' --header 'Accept: application/json' --header 'Authorization: <TOKEN>' 'https://api.fabulator.io/example/v1/update/111111111/111111111111'
```

### /example/v1/update/{iddomain}/{id}
---
##### ***PUT***
**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| iddomain | path |  | Yes | string |
| id | path |  | Yes | string |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| default | Successful | string |

```
curl -X PATCH --header 'Content-Type: application/json' --header 'Accept: application/json' --header 'Authorization: <TOKEN>' 'https://api.fabulator.io/example/v1/update/1111111/11111111/field_name/new%20value'
```

### /example/v1/update_json/{iddomain}/{id}
---
##### ***PUT***
**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| iddomain | path |  | Yes | string |
| id | path |  | Yes | string |
| body | body |  | No | [Model 14](#model-14) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| default | Successful | string |

```
curl -X PUT --header 'Content-Type: application/json' --header 'Accept: application/json' --header 'Authorization: <TOKEN>' -d '{
  "json": {}
}' 'https://api.fabulator.io/example/v1/update_json/11111111/111111111111'
```

### /example/v1/update/{iddomain}/{id}/{field}/{value}
---
##### ***PATCH***
**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| iddomain | path |  | Yes | string |
| id | path |  | Yes | string |
| field | path |  | Yes | string |
| value | path |  | Yes | string |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| default | Successful | string |

```
curl -X PATCH --header 'Content-Type: application/json' --header 'Accept: application/json' --header 'Authorization: <TOKEN>' 'https://api.fabulator.io/example/v1/update/1111111/11111111/field_name/new%20value'
```
