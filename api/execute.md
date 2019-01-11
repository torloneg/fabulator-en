Fabulator API
=============
Endpoint Execute


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

```
curl -X POST --header 'Content-Type: application/json' --header 'Accept: application/json' --header 'Authorization: <TOKEN>' -d '{
  "data": {}
}' 'https://api.fabulator.io/execute/v1/rule/<idrule>'
```
