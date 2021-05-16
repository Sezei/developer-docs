# Authentication

On Hyra, we use various types of authentication to allow access to resources across our systems. Our private APIs use ephemeral session tokens, that need to be regenerated periodically, thus are not suitable for usage in an API.

When authenticating with APIs provided in this documentation, you should use your API Key \(formerly called a token\). This API will not change, unless you request it to be rotated. 

You should send this API Key over in a Header named `Authorization`. There is no prefix or suffix on this header, so you do not need to include a prefix like a `Bearer`

