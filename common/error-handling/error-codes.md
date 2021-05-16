---
description: This page explains the codes which can be sent back in our errors array.
---

# Error Codes

| Code | Descriptor |
| :--- | :--- |
| not\_found | Content not found |
| internal\_error | An internal server error occurred |
| service\_unavailable | This service is currently unavailable |
| bad\_request | The data sent to the service was badly formatted |
| forbidden | Access to this content was forbidden |
| gone | Indicates that this service has been removed permanently. |
| upgrade\_required | The API version must be upgraded |
| too\_many\_requests | You are sending too many requests to Hyra |
| im\_a\_teapot | I'm a little teapot, Short and stout  |
| too\_early |  Try this request again later. `retry_after` will also be sent |
| bad\_gateway | Invalid response received from upstream |

Please refer to the table above when referencing errors.

