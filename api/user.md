Fabulator API
=============
Endpoint User

**Version:** 1.0.0

### Security
---
**bearer**  

|apiKey|*API Key*|
|---|---|
|Name|Authorization|
|In|header|

**<TOKEN>** value returned by the authentication function

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

```
curl -X GET --header 'Accept: application/json' --header 'Authorization: <TOKEN>' 'https://api.fabulator.io/users/v1/info/5ace3f349fc9355398e0ea8d'
```

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

```
curl -X POST --header 'Content-Type: application/json' --header 'Accept: application/json' --header 'Authorization: <TOKEN>' -d '{
  "email": "demo3@gmail.com",
  "password": "demo3-pwd192345",
  "first_name": "demo3",
  "last_name": "user demo",
  "role": "user"
}' 'https://api.fabulator.io/users/v1/add'
```



### /users/v1/query/{skip}/{limit}
---
##### ***POST***
**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| skip | path |  | Yes | number |
| limit | path |  | Yes | number |
| body | body |  | No | [Model 12](#model-12) |

```
curl -X POST --header 'Content-Type: application/json' --header 'Accept: application/json' --header 'Authorization: <AUTHTOKEN>' -d '{
  "select": "{}",
  "order": {
    "field": "date_update",
    "dir": 1
  },
  "query": "{\"role\":\"user\"}"
}' 'https://api.fabulator.io/users/v1/query/0/30'
```


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

```
curl -X DELETE --header 'Accept: application/json' --header 'Authorization: <TOKEN>' 'https://api.fabulator.io/users/v1/1111111111111111'
```

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

```
curl -X POST --header 'Content-Type: application/json' --header 'Accept: application/json'  -d '{
  "email": "demo3@gmail.com",
  "password": "pwd"
}' 'https://api.fabulator.io/users/v1/login'
```

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

```
curl -X POST --header 'Content-Type: application/json' --header 'Accept: application/json' --header 'Authorization: <TOKEN>' -d '{
  "password": "test"
}' 'https://api.fabulator.io/users/v1/reset_password/1111111'
```


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

```
curl -X POST --header 'Content-Type: application/json' --header 'Accept: application/json' --header 'Authorization: <TOKEN>' 'https://api.fabulator.io/users/v1/send_password_reminder/demo3%40gmail.com'
```

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

```
curl -X PUT --header 'Content-Type: application/json' --header 'Accept: application/json' --header 'Authorization: <TOKEN>' -d '{
  "first_name": "new first name",
  "last_name": "new last name",
  "role": "user"
}' 'https://api.fabulator.io/users/v1/update/11111111111111111111'
```

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

```
curl -X PATCH --header 'Content-Type: application/json' --header 'Accept: application/json' --header 'Authorization:  <TOKEN>' 'https://api.fabulator.io/users/v1/update/11111111111111111/first_name/new%20value'
```
