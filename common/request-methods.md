---
description: The methods that we use for our APIS
---

# Request Methods

When sending requests, please ensure you use the correct method type, in accordance with the HTTP protocol. 

* **GET** - Used to fetch from Hyra related resources and perform queries. This does not allow for modification of data \(create, update, delete\).
* **POST** - Used to create or update resources. 
* **DELETE** - Used to delete resources.

Responses are now encoded with standard HTTP response codes, such as 500 for a server error. Please see the errors section for information on how we handle errors. If multiple errors occur, we will send these back in the errors array. 

In some cases we may cache certain directives, where suitable.

Although advised, the `Accept` header is not required, and JSON is assumed for every response.

The `Content-Type` header should be used to indicate the format of the submitted data via `POST` requests.



