# Weather

{% api-method method="post" host="http://onyx-ip" path="/api/weather/daily" %}
{% api-method-summary %}
Get Weather
{% endapi-method-summary %}

{% api-method-description %}
Get all weather data
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-form-data-parameters %}
{% api-method-parameter name="token" type="string" required=true %}
Weather Token \( DarkAPI \)
{% endapi-method-parameter %}

{% api-method-parameter name="longitude" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="latitude" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-form-data-parameters %}
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

{% api-method method="post" host="http://onyx-ip" path="/api/weather/set\_token" %}
{% api-method-summary %}
Set Token
{% endapi-method-summary %}

{% api-method-description %}
Set the DarkAPI token
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-form-data-parameters %}
{% api-method-parameter name="weather\_token" type="string" required=true %}

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

