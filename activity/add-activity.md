---
description: Hyra's API allows you to add activity to users.
---

# Add Activity

### Example Use Cases

This API could be used to add more minutes onto a user, for example for a booster period in game.

{% api-method method="post" host="https://api.hyra.io" path="/v2/activity" %}
{% api-method-summary %}
Add activity to a user
{% endapi-method-summary %}

{% api-method-description %}
Fire a POST request to add minutes onto a user
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Your API Key
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="workspace" type="string" required=true %}
The ID of the Workspace
{% endapi-method-parameter %}

{% api-method-parameter name="userId" type="number" required=true %}
The numerical ID of the user \(Roblox ID\)
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="minutes" type="number" required=true %}
Amount of minutes to add
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Returns successfully response
{% endapi-method-response-example-description %}

```javascript
{
    type: "success",
    success: true,
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

