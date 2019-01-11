Fabulator API
=============
Endpoint Parser

**Version:** 1.0.0


### Security
---
**bearer**  

|apiKey|*API Key*|
|---|---|
|Name|Authorization|
|In|header|

**<TOKEN>** value returned by the authentication function


### /parser/v1/rule/{idrule}
---
##### ***POST***
**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| default | Successful | string |

```
curl -X POST \
  http://api.fabulator.io/parser/v1/rule/5a4d069498fefa6f148aaaa2 \
  -H 'Authorization: Bearer <TOKEN>' \
  -H 'Content-Type: text/plain' \
  -H 'Postman-Token: e3bf1c99-2fc1-4979-a3d7-076201454afe' \
  -H 'cache-control: no-cache' \
  -d '{% if data.string == '\''Feature'\''  %}
  data.string == '\''Feature'\''
{% endif %}

{% text clear="cr,lf"%}
  {{ 12 | Money.Convert("EUR","USD")  }}   
{% endtext %}'
```
