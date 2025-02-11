---
editable: false
---

# GEOINFO



#### Syntax {#syntax}


```
GEOINFO( address, scale )
```

#### Description {#description}
Converts `address` to geographical name corresponding to the specified `scale`.

Possible values for `scale` parameter:
- `"country"`;
- `"country_code"`;
- `"region"`;
- `"locality"`.

To enable the function, go to the [Service Settings](https://datalens.yandex.com/settings) page.

**Argument types:**
- `address` — `String`
- `scale` — `String`


**Return type**: `String`

{% note info %}

Only constant values are accepted for arguments (`scale`).

{% endnote %}


#### Examples {#examples}

```
GEOINFO("посёлок Свободный Серп", "country") = "Россия"
```


#### Data source support {#data-source-support}

`Materialized Dataset`.
