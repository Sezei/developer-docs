---
description: Change a users rank in a group directly to a specified rank
---

# Promote a user

{% api-method method="patch" host="https://api.hyra.io/v2" path="/group/rank" %}
{% api-method-summary %}
Change a users rank
{% endapi-method-summary %}

{% api-method-description %}
This API endpoint will allow you to change a users rank programmatically in a Roblox group. You can use this to promote users or demote them based on events or logic. 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Your API Key
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-query-parameters %}
{% api-method-parameter name="userId" type="number" required=true %}
The numerical ID of the user \(Roblox ID\)
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="rank" type="number" required=true %}
The rank ID from the Roblox Group Admin to promote the user to
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successful response
{% endapi-method-response-example-description %}

```javascript
{
    "type": "success",
    "success": true
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
User on Roblox is not found or is not in the Roblox Group
{% endapi-method-response-example-description %}

```javascript
{
    "type": "error",
    "error": {
        "code": "not_found",
        "message": "User not found"
    }
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=500 %}
{% api-method-response-example-description %}
An internal server error occurred - contact Hyra Support
{% endapi-method-response-example-description %}

```javascript
{
    "type": "error",
    "error": {
        "code": "internal",
        "message": "An internal error occured"
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

