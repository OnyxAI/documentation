# Calendar

{% api-method method="get" host="http://onyx-ip" path="/api/calendar" %}
{% api-method-summary %}
Get events
{% endapi-method-summary %}

{% api-method-description %}
Get all events
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

```javascript
[
    {...}
]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="http://onyx-ip" path="/api/calendar" %}
{% api-method-summary %}
Add Event
{% endapi-method-summary %}

{% api-method-description %}
Add an event
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-form-data-parameters %}
{% api-method-parameter name="end" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="start" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="color" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="lieu" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="notes" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="title" type="string" required=false %}

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

{% api-method method="put" host="http://onyx-ip" path="/api/calendar" %}
{% api-method-summary %}
Update Date
{% endapi-method-summary %}

{% api-method-description %}
Update Date
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-form-data-parameters %}
{% api-method-parameter name="id" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="end" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="start" type="string" required=true %}

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

{% api-method method="post" host="http://onyx-ip" path="/api/calendar" %}
{% api-method-summary %}
Update event
{% endapi-method-summary %}

{% api-method-description %}
Update an event
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

{% api-method-form-data-parameters %}
{% api-method-parameter name="color" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="lieu" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="notes" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="title" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="delete" type="boolean" required=false %}

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

