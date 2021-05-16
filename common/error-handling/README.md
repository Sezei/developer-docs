# Error Handling

In the event that a request does not go through successfully, we will send back a response with the relevant [status code](https://en.wikipedia.org/wiki/List_of_HTTP_status_codes). `200` indicates a successful request.

When responding with an error, we will send over a `type` key being `error` as well as a the relevant status code. We will send over the error\(s\) in an array.

An example error response can be seen below

```javascript
{
    "type": "error",
    "errors": [
        {
            "code": "not_found",
            "message": "User Not Found"
        }
    ]
}
```

Please see documentation on the error codes below.

{% page-ref page="error-codes.md" %}

In some rare cases we may also send over an `advanced_debug` value in the errors array object. This will contain a more advanced root error. This will be formatted as string, and does not follow a specific structure.This key is typically only sent when a `500` `internal_error` occurs.



