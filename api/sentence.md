Fabulator API
=============
Endpoint Sentence

**Version:** 1.0.0


### Security
---
**bearer**  

|apiKey|*API Key*|
|---|---|
|Name|Authorization|
|In|header|

**<TOKEN>** value returned by the authentication function



### /sentence/v1/{idrule}/{id}
---
##### ***DELETE***
**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| idrule | path |  | Yes | string |
| id | path |  | Yes | string |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| default | Successful | string |

curl -X DELETE --header 'Accept: application/json' --header 'Authorization: <TOKEN>' 'https://api.fabulator.io/sentence/v1/<idrule>/<id>'

### /sentence/v1/info/{idrule}/{id}
---
##### ***GET***
**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| idrule | path |  | Yes | string |
| id | path |  | Yes | string |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| default | Successful | string |

```
curl -X GET --header 'Accept: application/json' --header 'Authorization: <TOKEN>' 'https://api.fabulator.io/sentence/v1/info/<idrule>/<id>'
```
### /sentence/v1/add/{idrule}
---
##### ***POST***
**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| idrule | path |  | Yes | string |
| body | body |  | No | [Model 7](#model-7) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| default | Successful | string |

```
curl -X POST --header 'Content-Type: application/json' --header 'Accept: application/json' --header 'Authorization: <TOKEN>' -d '{
  "name": "string",
  "text": "string",
  "position": 0,
  "status": 0
}' 'https://api.fabulator.io/sentence/v1/add/<idrule>'
```

### /sentence/v1/update/{idrule}/{id}
---
##### ***PUT***
**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| idrule | path |  | Yes | string |
| id | path |  | Yes | string |
| body | body |  | No | [Model 15](#model-15) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| default | Successful | string |

```
curl -X PUT --header 'Content-Type: application/json' --header 'Accept: application/json' --header 'Authorization: <TOKEN>' -d '{
  "name": "string",
  "text": "string",
  "note": "string",
  "status": 0
}' 'https://api.fabulator.io/sentence/v1/update/<idrule>/<id>'
```
