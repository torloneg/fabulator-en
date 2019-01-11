Fabulator API
=============
Endpoint Rule


### Security
---
**bearer**  

|apiKey|*API Key*|
|---|---|
|Name|Authorization|
|In|header|

**<TOKEN>** value returned by the authentication function


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
