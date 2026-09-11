---
description: Data stays until you close the tab
icon: database
---

# Session Storage

{% code overflow="wrap" %}
```
sessionStorage.setItem("name", "John");
```
{% endcode %}



{% code overflow="wrap" %}
```
const name = sessionStorage.getItem("name");
```
{% endcode %}



delete one

{% code overflow="wrap" %}
```
sessionStorage.removeItem("name");
```
{% endcode %}

delete all

{% code overflow="wrap" %}
```
sessionStorage.clear();
```
{% endcode %}
