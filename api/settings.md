---
description: Settings API
---

# Settings

{% api-method method="get" host="http://onyx-url" path="/api/settings/get\_onyx\_data" %}
{% api-method-summary %}
Get Onyx Data
{% endapi-method-summary %}

{% api-method-description %}
Download or Update Onyx Data
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Token
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
    "status": "success"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

