Fabulator API
=============
Endpoint Fabulator project

**Version:** 1.0.0

**Contact information:**  
Torlone Gianfranco  
https://twitter.com/torloneg  
torloneg@gmail.com  

### Security
---
**bearer**  

|apiKey|*API Key*|
|---|---|
|Name|Authorization|
|In|header|

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

### /rule/v1/info/{id}
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

### /schema/v1/info/{id}
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

### /users/v1/info/{id}
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

### /users/v1/add
---
##### ***POST***
**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| body | body |  | No | [Model 2](#model-2) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| default | Successful | string |

### /users/v1/login
---
##### ***POST***
**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| body | body |  | No | [Model 3](#model-3) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| default | Successful | string |

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

### /execute/v1/rule/{idrule}
---
##### ***POST***
**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| idrule | path |  | Yes | string |
| body | body |  | No | [Model 5](#model-5) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| default | Successful | string |

### /parser/v1/rule/{idrule}
---
##### ***POST***
**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| default | Successful | string |

### /rule/v1/add/{iddomain}
---
##### ***POST***
**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| iddomain | path |  | Yes | string |
| body | body |  | No | [Model 6](#model-6) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| default | Successful | string |

### /schema/v1/group/{type}
---
##### ***POST***
**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| type | path |  | Yes | string |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| default | Successful | string |

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

### /users/v1/reset_password/{token}
---
##### ***POST***
**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| token | path |  | Yes | string |
| body | body |  | No | [Model 8](#model-8) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| default | Successful | string |

### /users/v1/send_password_reminder/{email}
---
##### ***POST***
**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| email | path |  | Yes | string |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| default | Successful | string |

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

### /execute/v1/local/{domain}/{key}
---
##### ***POST***
**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| domain | path |  | Yes | string |
| key | path |  | Yes | string |
| body | body |  | No | [Model 5](#model-5) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| default | Successful | string |

### /schema/v1/query/{skip}/{limit}
---
##### ***POST***
**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| skip | path |  | Yes | number |
| limit | path |  | Yes | number |
| body | body |  | No | [Model 11](#model-11) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| default | Successful | string |

### /users/v1/query/{skip}/{limit}
---
##### ***POST***
**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| skip | path |  | Yes | number |
| limit | path |  | Yes | number |
| body | body |  | No | [Model 12](#model-12) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| default | Successful | string |

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

### /execute/v1/rule/{idrule}/example/{idexample}
---
##### ***POST***
**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| idrule | path |  | Yes | string |
| idexample | path |  | Yes | string |
| idsentence | query |  | No | string |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| default | Successful | string |

### /rule/v1/query/{iddomain}/{skip}/{limit}
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

### /rule/v1/{id}
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

### /users/v1/{id}
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

### /example/v1/{iddomain}/{id}
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

### /users/v1/update/{id}
---
##### ***PUT***
**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path |  | Yes | string |
| body | body |  | No | [Model 13](#model-13) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| default | Successful | string |

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

### /rule/v1/update/{iddomain}/{id}
---
##### ***PUT***
**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path |  | Yes | string |
| iddomain | path |  | Yes | string |
| body | body |  | No | [Model 6](#model-6) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| default | Successful | string |

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

### /rule/v1/update/{id}/{field}/{value}
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

### /users/v1/update/{id}/{field}/{value}
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

### Models
---

### Model 1  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| name | string |  | Yes |
| description | string |  | Yes |
| color | string |  | Yes |
| language | string |  | Yes |
| status | number |  | Yes |

### Model 2  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| email | string |  | Yes |
| password | string |  | Yes |
| first_name | string |  | Yes |
| last_name | string |  | Yes |
| role | string |  | Yes |

### Model 3  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| email | string |  | Yes |
| password | string |  | Yes |

### json  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| json | object |  |  |

### Model 4  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| name | string |  | Yes |
| description | string |  | No |
| json | [json](#json) |  | Yes |

### Model 5  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| data | [json](#json) |  | No |

### Model 6  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| name | string |  | Yes |
| note | string |  | No |
| status | number |  | Yes |

### Model 7  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| name | string |  | Yes |
| text | string |  | Yes |
| position | number |  | Yes |
| status | number |  | Yes |

### Model 8  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| password | string |  | Yes |

### order  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| field | string |  | Yes |
| dir | number |  | Yes |

### Model 9  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| select | string |  | Yes |
| order | [order](#order) |  | No |
| query | string |  | Yes |

### Model 10  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| field | string |  | Yes |
| dir | number |  | Yes |

### Model 11  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| select | string |  | Yes |
| order | [Model 10](#model-10) |  | No |
| query | string |  | Yes |

### Model 12  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| select | string |  | Yes |
| order | [order](#order) |  | No |
| query | string |  | Yes |

### Model 13  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| first_name | string |  | Yes |
| last_name | string |  | Yes |
| role | string |  | No |

### Model 14  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| json | [json](#json) |  | Yes |

### Model 15  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| name | string |  | Yes |
| text | string |  | No |
| note | string |  | No |
| status | number |  | Yes |