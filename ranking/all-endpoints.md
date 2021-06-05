---
description: All available endpoints on Hyra Ranking
---

# All endpoints

{% api-method method="post" host="https://ranking.hyra.io" path="/token" %}
{% api-method-summary %}
Create a token
{% endapi-method-summary %}

{% api-method-description %}
Create a Hyra Ranking token
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="content-type" type="string" required=true %}
text/json
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="cookie" type="string" required=true %}
The .ROBLOSECURITY cookie
{% endapi-method-parameter %}

{% api-method-parameter name="groupId" type="integer" required=true %}
The ID of the Group
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{ 
    "success": true, 
    "token": "XXXXXXXXXXXXXXXXXXXXXXX", 
    "username": "Roblox", 
    "id": 1
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="put" host="https://ranking.hyra.io" path="/spin" %}
{% api-method-summary %}
Spin token
{% endapi-method-summary %}

{% api-method-description %}
Roll the token, and regenerate a new one
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="content-type" type="string" required=true %}
text/json
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="token" type="string" required=true %}
The Hyra Ranking token
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "success": true,
    "token": "XXXXXXXXXXXXXXXX"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="delete" host="https://ranking.hyra.io" path="/token/{token}" %}
{% api-method-summary %}
Delete token
{% endapi-method-summary %}

{% api-method-description %}
Delete supplied token from system, invalidating it entirely
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="token" type="string" required=true %}
The Hyra Ranking token
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
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

{% api-method method="post" host="https://ranking.hyra.io" path="/rank" %}
{% api-method-summary %}
Rank User
{% endapi-method-summary %}

{% api-method-description %}
Rank a user to the specified rank in the specified group
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="content-type" type="string" required=true %}
text/json
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="token" type="string" required=true %}
The Hyra Ranking token
{% endapi-method-parameter %}

{% api-method-parameter name="rankNumber" type="string" required=true %}
The rank in the group which user should be ranked to \(1-253 supported\)
{% endapi-method-parameter %}

{% api-method-parameter name="targetId" type="string" required=true %}
The Roblox Player ID of the user you are ranking
{% endapi-method-parameter %}

{% api-method-parameter name="groupId" type="string" required=true %}
The group ID of where you are promoting the user
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
  "Success": true,
  "Message": "Successfully changed rank of user"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://ranking.hyra.io" path="/message" %}
{% api-method-summary %}
Message User
{% endapi-method-summary %}

{% api-method-description %}
Message specified Roblox User
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="content-type" type="string" required=true %}
text/json
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="token" type="string" required=true %}
The Hyra Ranking token
{% endapi-method-parameter %}

{% api-method-parameter name="subject" type="string" required=true %}
The subject of the message
{% endapi-method-parameter %}

{% api-method-parameter name="message" type="string" required=true %}
The contents of the message
{% endapi-method-parameter %}

{% api-method-parameter name="targetId" type="string" required=true %}
The Roblox Player Id of the user you are messaging
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "Success": true,
    "Message": "Successfully messaged user",
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://ranking.hyra.io" path="/token/{token}" %}
{% api-method-summary %}
Get token usage & information
{% endapi-method-summary %}

{% api-method-description %}
Gets usage and information about the specified token
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="token" type="string" required=true %}
The Hyra Ranking token
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "success": true,
    "created": {
        "_nanoseconds": 966000000
        "_seconds": 1606651106
    },
    "groupId": 1,
    "paid": false,
    "usage": 0
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://ranking.hyra.io" path="/logs/{token}" %}
{% api-method-summary %}
Retrieve logs
{% endapi-method-summary %}

{% api-method-description %}
Will return an array of logs, sorted by date of log, descending.   
  
Supports optional cursor query to index the pages.  
  
Returns maximum of 20 logs per page.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="token" type="string" required=true %}
The Hyra Ranking token
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-query-parameters %}
{% api-method-parameter name="index" type="string" required=false %}
The ID of the index in logs to startAfter. Typically the last index on the first query.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "success": true,
    "data": [{
        "id": "XXXXXXXXXXXXXXXXXXX",
        "data": {
            "country": "US",
            "date": {
                "_nanoseconds": 995000000
                "_seconds": 1607018400
            },
            "groupId": 1,
            "ip": 1.1.1.1,
            "rankId": 250,
            "ray": "5fbf2f4569837171-ORD",
            "type": "Hyra Browser",
            "user": "1"
        }
    }],
    "length": 1,
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

