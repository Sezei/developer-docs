---
description: >-
  A handy IP geolocation route, commonly used to locate Roblox servers, allowing
  you to select the most appropriate location for a CDN.
---

# Geo

This route will return information about the requesting IP address. We've changed the headers sent on this request to allow foreign origins to use it, which may make it useful for use within a site. 

{% api-method method="get" host="https://api.hyra.io" path="/geo" %}
{% api-method-summary %}
Get Geo
{% endapi-method-summary %}

{% api-method-description %}
Will return the IP Geo Data for the request IP
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
If success, will return `type` `ip` and an `ip` object. See below for an example.
{% endapi-method-response-example-description %}

```javascript
{
    "type": "ip",
    "ip": {
        "isp": "Hydra Communications Ltd",
        "accuracy": 1000,
        "timezone": "Europe/London",
        "location": {
            "longitude": "-2.5917",
            "latitude": "51.4535",
            "continent_code:" "EU",
            "country_code:" "GB",
            "city": "Bristol",
            "country": "United Kingdom",
            "region": "England"
        },
        "ip": "77.81.191.180"
    }
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=500 %}
{% api-method-response-example-description %}
Something went wrong
{% endapi-method-response-example-description %}

```javascript
{
    "type": "error",
    "errors": [
        {
            "code": "internal_error",
            "message:" "Something went wrong."
        }
    ]
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=503 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "type": "error",
    "errors": [
        {
            "code": "service_unavailable",
            "message:" "This service is unavailable."
        }
    ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

