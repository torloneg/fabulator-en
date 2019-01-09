Fabulator API
=============
Endpoint Fabulator project

**Version:** 1.0.0

**Contact information:**  
Torlone Gianfranco  
https://twitter.com/torloneg  
torloneg@gmail.com  



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