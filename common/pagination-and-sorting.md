---
description: The use of cursors is required for heavy APIs
---

# Pagination & Sorting

Directives which require pagination are indicated using a notice like below.

{% hint style="info" %}
This directive requires pagination
{% endhint %}

You will need to specify a cursor to utilise the API. If a cursor is not provided, we will use the first cursor. The next page cursor can be found by utilising the `next_page_cursor` which is sent on the body of the first response. 

If you wish to sort data that requires pagination, please use the `sort` parameter. You can specify to sort either:

* **desc** - descending
* **asc** - ascending

### Good to know

* When sorting text fields, they will be sorted by alphabetical order.
* When sorting number fields, they will be sorted by the size of the number
* When sorting timestamp fields, they will be sorted by the 

