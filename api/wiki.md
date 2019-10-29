# Wiki

{% api-method method="post" host="http://onyx-ip" path="/api/wiki" %}
{% api-method-summary %}
Get Wiki
{% endapi-method-summary %}

{% api-method-description %}
Get summary and description of an article
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-form-data-parameters %}
{% api-method-parameter name="search" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="lang" type="string" required=true %}
en, fr
{% endapi-method-parameter %}
{% endapi-method-form-data-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{"status": "success", "url": "url", "title": "title", "summary": "summary"}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

