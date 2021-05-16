# Promote a user

{% hint style="danger" %}
This route is not currently active
{% endhint %}

{% api-method method="patch" host="https://api.hyra.io/v2" path="/group/promote" %}
{% api-method-summary %}
Promote a user to the next rank
{% endapi-method-summary %}

{% api-method-description %}
PI endpoint will allow you to change a users rank programmatically in a Roblox group. You can use this to promote users or demote them based on events or logic. 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Your API Key
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="userId" type="number" required=true %}
The numerical ID of the user \(Roblox ID\)
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "type": "success",
    "success": true
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

