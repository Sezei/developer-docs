---
description: Hyra's API allows you to remove activity from users.
---

# Remove Activity

### Example Use Cases

This API can can remove minutes, which could be used to remove activity from users who are AFK in game.

{% api-method method="delete" host="https://api.hyra.io" path="/activity" %}
{% api-method-summary %}

{% endapi-method-summary %}

{% api-method-description %}
Fire a DELETE request to remove activity
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
Amount of minutes to remove
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Returns successful response
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

