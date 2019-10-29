# House

{% api-method method="get" host="http://onyx-ip" path="/api/house" %}
{% api-method-summary %}
Get houses
{% endapi-method-summary %}

{% api-method-description %}
Get all houses
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
token
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
[
    {...}
]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="http://onyx-ip" path="/api/house/add" %}
{% api-method-summary %}
Add house
{% endapi-method-summary %}

{% api-method-description %}
Add a house
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-form-data-parameters %}
{% api-method-parameter name="longitude" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="latitude" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="country" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="postal" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="city" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="address" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="name" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-form-data-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "status": "success"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="http://onyx-ip" path="/api/house/delete/<id>" %}
{% api-method-summary %}
Delete house
{% endapi-method-summary %}

{% api-method-description %}
Delete a house
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
token
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "status": "success"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

