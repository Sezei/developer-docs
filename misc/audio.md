---
description: Get audio from the Roblox catalog
---

# Audio

{% api-method method="get" host="https://api.hyra.io" path="/audio/:soundId" %}
{% api-method-summary %}
Get sound
{% endapi-method-summary %}

{% api-method-description %}
This will return the sound data of a given audio in MP3 format.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="soundId" type="integer" required=true %}
The numerical Roblox Sound ID
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Returns the audio
{% endapi-method-response-example-description %}

```
No response example is available for this method
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Audio not found
{% endapi-method-response-example-description %}

```
An empty response is returned
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

