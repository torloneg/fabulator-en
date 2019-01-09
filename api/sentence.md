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



