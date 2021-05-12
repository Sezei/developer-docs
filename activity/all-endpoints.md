---
description: All available endpoints on Hyra Activity
---

# All endpoints

{% hint style="danger" %}
These APIs are for internal use and not intended for public consumption. These APIs may be deprecated at any time and are not covered under SLA.
{% endhint %}

{% api-method method="get" host="https://m1.hyra.cloud" path="/activity-info" %}
{% api-method-summary %}
Get Activity Information
{% endapi-method-summary %}

{% api-method-description %}
Return ranking and group information for activity
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="authorization" type="string" required=true %}
Auth bearer token
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "success": true,
    "groupId": 1,
    "minRank": 30
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://m1.hyra.cloud" path="/start-activity" %}
{% api-method-summary %}
Start Activity
{% endapi-method-summary %}

{% api-method-description %}
Starts an activity tracker for given player
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="content-type" type="string" required=true %}
text/json
{% endapi-method-parameter %}

{% api-method-parameter name="authorization" type="string" required=true %}
Auth bearer token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="PlayerId" type="integer" required=true %}

{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "success": true
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



{% api-method method="post" host="https://m1.hyra.cloud" path="/activity-info" %}
{% api-method-summary %}

{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="content-type" type="string" required=true %}
text/json
{% endapi-method-parameter %}

{% api-method-parameter name="authorization" type="string" required=true %}
Auth bearer token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="PlayerId" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```java
{
    "success": true
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

