---
description: Neurons API
---

# Neurons

{% api-method method="get" host="http://onyx-url" path="/api/neurons/get\_all" %}

{% api-method method="get" host="http://onyx-url" path="/api/neurons/get\_store\_list" %}
{% api-method-summary %}

{% endapi-method-summary %}

{% api-method-description %}
Getting all neurons of the store
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
    "status": "success",
    "neurons": []
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="http://onyx-url" path="/api/neurons/install" %}
{% api-method-summary %}
Install Neuron
{% endapi-method-summary %}

{% api-method-description %}
Install a neuron
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-form-data-parameters %}
{% api-method-parameter name="name" type="string" required=true %}
Neuron raw name
{% endapi-method-parameter %}

{% api-method-parameter name="url" type="string" required=true %}
Neuron git url
{% endapi-method-parameter %}
{% endapi-method-form-data-parameters %}
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

{% api-method method="post" host="http://onyx-url" path="/api/neurons/remove" %}
{% api-method-summary %}
Remove Neuron
{% endapi-method-summary %}

{% api-method-description %}
Remove a neuron
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-form-data-parameters %}
{% api-method-parameter name="name" type="string" required=true %}
Neuron raw name
{% endapi-method-parameter %}
{% endapi-method-form-data-parameters %}
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

