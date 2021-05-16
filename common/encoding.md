---
description: How our APIS are encoded
---

# Encoding

All API data is encoded as defined by JSON in [RFC4627](http://www.ietf.org/rfc/rfc4627.txt). The default encoding for APIs is UTF-8. Certain characters \(i.e. emojis\) may be handled as surrogate unicode pairs. 

When contacting our APIs, some query parameters may need to be [URL encoded](http://en.wikipedia.org/wiki/Percent-encoding) when sending, for example a text string with spaces should have the string encoded with "%20" instead of " "

Dates are encoded as timestamps, so are sent via JSON in the following format, in this example the key on the object is `date`.

```javascript
date: {
    _nanoseconds: 331000000,
    _seconds: 1608559015
}
```

**`_seconds`** = The number of seconds of UTC time since Unix epoch 1970-01-01T00:00:00Z.

**`_nanoseconds`** = The non-negative fractions of a second at nanosecond resolution. Negative second values with fractions must still have non-negative nanoseconds values that count forward in time.

If you are looking for an easy way to convert our timestamps into a Javascript time, to to a second accuracy, please use:

```javascript
new Date(date._seconds * 1000) // Converts to Javascript Date Object
```

If you are looking for more precise approximate accuracy, please use  the following:

```javascript
new Date((data._seconds + (data._nanoseconds * 1e-9)) * 1000) // 1e-9 is equal to 1 × 10⁻⁹
```

When sending dates back to our server in the form of a `POST` request, please convert to them to ISO String following [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601).

You can do this in Javascript using the following

```javascript
/*
** new Date() will return the current system date
** .toISOString() will convert the date object to an ISO String formatted date.
** Due to the nature of the ISO String, it will always be outputted in UTC
*/

new Date().toISOString()
```

You can do this in Roblox Lua using the following:

```lua
local dt = DateTime.now()

dt:ToIsoDate()
```

