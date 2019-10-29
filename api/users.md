---
description: User API
---

# Users

{% api-method method="get" host="http://onyx-ip" path="/api/users" %}
{% api-method-summary %}
Get Users
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get all users.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
Authentication token
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```javascript
[
    {
        "username": "User",
        "email": "mail@user.com"
        ...
    }
]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="http://onyx-ip" path="/api/get\_access\_token" %}
{% api-method-summary %}
Get Access token
{% endapi-method-summary %}

{% api-method-description %}
Get you access token with your refresh token
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Refresh token
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Getting access token
{% endapi-method-response-example-description %}

```javascript
{
    "access_token": "token"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="http://onyx-ip" path="/api/user/register" %}
{% api-method-summary %}
Register User
{% endapi-method-summary %}

{% api-method-description %}
Register a new user
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-form-data-parameters %}
{% api-method-parameter name="verifpassword" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="password" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="email" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="username" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-form-data-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "status": "success"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="http://onyx-ip" path="/api/user/login" %}
{% api-method-summary %}
Login User
{% endapi-method-summary %}

{% api-method-description %}
Login a user
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-form-data-parameters %}
{% api-method-parameter name="password" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="email" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-form-data-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "status": "success",
    "access_token": "token",
    "refresh_token": "token"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="http://onyx-ip" path="/api/user/logout\_access" %}
{% api-method-summary %}
Logout Access
{% endapi-method-summary %}

{% api-method-description %}
Revoke an access token
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
access\_token
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "status": "success"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="http://onyx-ip" path="/api/user/logout\_refresh" %}
{% api-method-summary %}
Logout Refresh
{% endapi-method-summary %}

{% api-method-description %}
Revoke a refresh token
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
refresh token
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "status": "success"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="http://onyx-ip" path="/api/user/delete/<id>" %}
{% api-method-summary %}
Delete Account
{% endapi-method-summary %}

{% api-method-description %}
Admin : Delete an account
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
Account id
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Admin token
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "status": "success"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="http://onyx-ip" path="/api/user/manage/<id>" %}
{% api-method-summary %}
Manage User
{% endapi-method-summary %}

{% api-method-description %}
Admin : Manage a user account
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
Account id
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Admin token
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "status": "success"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="http://onyx-ip" path="/api/user/change" %}
{% api-method-summary %}
Modify Account
{% endapi-method-summary %}

{% api-method-description %}
Modify account information
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-form-data-parameters %}
{% api-method-parameter name="password" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="username" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="email" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="lastpassword" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-form-data-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "status": "success"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

