---
description: >-
  The credibility API allows you to fetch the credibility of a given user using
  our Community Standing database.
---

# Credibility

## Usage

{% api-method method="get" host="https://api.hyra.io" path="/credibility" %}
{% api-method-summary %}
Fetch a users credibility
{% endapi-method-summary %}

{% api-method-description %}
This method will fetch a users credibility and return it.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Your API token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="userId" type="string" required=true %}
Users Roblox ID \(Numerical\)
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
User was found, the data array will contain a reference to the information.
{% endapi-method-response-example-description %}

```javascript
{
    "type": "credibility",
    "data": [
        {
            date: {
                _nanoseconds: 331000000,
                _seconds: 1608559015
            },
            note: "Admin Abuse",
            media: ["https://uploads.hyra.io/credibility/1"]
        }
    ]
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
Badly Formatted Request
{% endapi-method-response-example-description %}

```javascript
{
    "type": "error",
    "errors": [
        {
            "code": "bad_request",
            "message": "Bad Request"
        }
    ]
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}
An invalid or expired API Authorization header was sent
{% endapi-method-response-example-description %}

```javascript
{
    "type": "error",
    "errors": [
        {
            "code": "forbidden",
            "message": "Invalid Auth"
        }
    ]
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
This user was not found in our credibility platform
{% endapi-method-response-example-description %}

```javascript
{
    "type": "error",
    "errors": [
        {
            "code": "not_found",
            "message": "User not found"
        }
    ]
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=500 %}
{% api-method-response-example-description %}
Internal Server Error
{% endapi-method-response-example-description %}

```javascript
{
    "type": "error",
    "errors": [
        {
            "code": "internal_error",
            "message": "Internal Server Error"
        }
    ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

## Pricing

This API is a billable endpoint. This API will use **1 Static Read** per invocation, totalling at 1 credit total usage.

