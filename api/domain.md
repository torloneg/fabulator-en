Fabulator API
=============
Endpoint Domain

**Version:** 1.0.0


### Security
---
**bearer**  

|apiKey|*API Key*|
|---|---|
|Name|Authorization|
|In|header|

**<TOKEN>** value returned by the authentication function

### /domain/v1/info/{id}
---
##### ***GET***
**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path |  | Yes | string |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| default | Successful | string |

```
curl -X GET --header 'Accept: application/json' --header 'Authorization: <TOKEN>' 'https://api.fabulator.io/domain/v1/info/11111111111111111'
```

### /domain/v1/add
---
##### ***POST***
**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| body | body |  | No | [Model 1](#model-1) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| default | Successful | string |

```
curl -X POST --header 'Content-Type: application/json' --header 'Accept: application/json' --header 'Authorization: <TOKEN>' -d '{
  "name": "string",
  "description": "string",
  "color": "string",
  "language": "it-IT",
  "status": 0
}' 'https://api.fabulator.io/domain/v1/add'
```

### /domain/v1/query/{skip}/{limit}
---
##### ***POST***
**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
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
}' 'https://api.fabulator.io/domain/v1/query/0/30'
```

### /domain/v1/{id}
---
##### ***DELETE***
**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path |  | Yes | string |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| default | Successful | string |

```
curl -X DELETE --header 'Accept: application/json' --header 'Authorization: <TOKEN>' 'https://api.fabulator.io/domain/v1/11111111111111'
```

### /domain/v1/update/{id}
---
##### ***PUT***
**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path |  | Yes | string |
| body | body |  | No | [Model 1](#model-1) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| default | Successful | string |

```
curl -X PUT --header 'Content-Type: application/json' --header 'Accept: application/json' --header 'Authorization: <TOKEN>' -d '{
  "name": "string",
  "description": "string",
  "color": "string",
  "language": "it-IT",
  "status": 0
}' 'https://api.fabulator.io/domain/v1/update/1111111111111'
```

### /domain/v1/update/{id}/{field}/{value}
---
##### ***PATCH***
**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path |  | Yes | string |
| field | path |  | Yes | string |
| value | path |  | Yes | string |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| default | Successful | string |

```
curl -X PATCH --header 'Content-Type: application/json' --header 'Accept: application/json' --header 'Authorization: <TOKEN>' 'https://api.fabulator.io/domain/v1/update/1111111111111111/field_name/value'
```
