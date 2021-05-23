---
description: Hyra's API allows you to fetch activity for a specific user.
---

# Get Activity

### Example Use Cases

This API could be used for various use cases, such as showing user activity in-game or on a Discord bot.

{% api-method method="get" host="https://api.hyra.io" path="/v2/activity" %}
{% api-method-summary %}
Get User Activity
{% endapi-method-summary %}

{% api-method-description %}
This API endpoint allows you to return the minutes for the given user since the last distribution.   
  
If the user is not found or they have no activity, this endpoint will always return 0.
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

{% api-method-parameter name="userId" type="string" required=true %}
The numerical ID of the user \(Roblox ID\)
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Users minutes since last distribution
{% endapi-method-response-example-description %}

```javascript
{
    type: "activity",
    minutes: 300
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

