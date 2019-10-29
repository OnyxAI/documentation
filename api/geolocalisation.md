# Geolocalisation

{% api-method method="get" host="http://onyx-ip" path="/api/geolocalisation" %}
{% api-method-summary %}
Get Geolocalisation
{% endapi-method-summary %}

{% api-method-description %}
Get latitude and longitude
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
{
    "status": "success",
    "latitude": "50",
    "longitude": "2"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

