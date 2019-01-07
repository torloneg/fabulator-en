---
description: Description of Money
---

# Money

## Money.Convert

converts the value of one currency into another

**params**

| name | type | description |
| :--- | :--- | :--- |
| input | string |  |
| from | string |  |
| to | string |  |

```text
example: {{ 123 | Money.Convert("USD","EUR") }}

output: 108,03
```

## Money.Symbol

returns the symbol of a currency

**params**

| name | type | description |
| :--- | :--- | :--- |
| input | string |  |

```text
example: {{ "USD" | Money.Symbol()}}

output: $
```

## Money.SymbolExt

TODO

**params**

| name | type | description |
| :--- | :--- | :--- |
| input | string |  |

```text
example: TODO

output: TODO
```

