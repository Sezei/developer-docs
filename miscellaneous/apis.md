# APIs

{% hint style="danger" %}
These APIs are for internal use and not intended for public consumption. These APIs may be deprecated at any time and are not covered under SLA.
{% endhint %}

{% api-method method="get" host="https://m1.hyra.cloud" path="/friends/{playerId}" %}
{% api-method-summary %}
Friends
{% endapi-method-summary %}

{% api-method-description %}
Returns friends of player
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="playerId" type="string" required=true %}
The Roblox User ID
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
   "0":{
      "isOnline":false,
      "isDeleted":true,
      "description":null,
      "created":"0001-01-01T06:00:00Z",
      "isBanned":false,
      "id":1024139217,
      "name":"Reset1024139217",
      "displayName":"Reset1024139217"
   },
   "1":{
      "isOnline":false,
      "isDeleted":true,
      "description":null,
      "created":"0001-01-01T06:00:00Z",
      "isBanned":false,
      "id":113771541,
      "name":"Nethatar",
      "displayName":"Nethatar"
   },
   "2":{
      "isOnline":false,
      "isDeleted":true,
      "description":null,
      "created":"0001-01-01T06:00:00Z",
      "isBanned":false,
      "id":277258,
      "name":"Nitros",
      "displayName":"Nitros"
   },
   "3":{
      "isOnline":false,
      "isDeleted":true,
      "description":null,
      "created":"0001-01-01T06:00:00Z",
      "isBanned":false,
      "id":93254638,
      "name":"Ananymoos",
      "displayName":"Ananymoos"
   },
   "success":true
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://m1.hyra.cloud" path="/avatar/{playerId}" %}
{% api-method-summary %}
Avatar
{% endapi-method-summary %}

{% api-method-description %}
Returns avatar in a high quality format, with proper content-type header.   
  
Not a proxy, just a REST API.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="playerId" type="string" required=true %}
The Roblox User ID
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
   "success":true,
   "url":"https://tr.rbxcdn.com/c3ee609e91804ee2f15c6375355a381a/352/352/AvatarHeadshot/png"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

