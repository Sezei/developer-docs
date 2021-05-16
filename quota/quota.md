# Quota & Usage

By default, each Workspace is given a free tier API key. This is great for use within a smaller environment that doesn't need to leverage the Hyra API as heavily.

Usage is tracked using a points based API call. Regardless of if your API call is successful, your quota will still be used up. 

### Dictionary of terms

| Term | Definition |
| :--- | :--- |
| Daily Limit | Your daily API limit for this type of request. Daily limits are reset at 00:00:00 America/New\_York time. |
| Static Read | A static read is a read from a Hyra proxy API. Typically this type of API is fetching data from a service. |
| Dynamic Read | A dynamic read is data that is read from the Hyra central database. Typically this could be reading information about a users activity or a similar system. |
| Dynamic Update | A dynamic update is updating or creating data that is stored in the Hyra central database. Typically this is ranking a user. |
| Dynamic Delete | A dynamic delete is removing data from the Hyra central database. This could be deleting an item from the logbook via the API. |

## Free tier

We offer a generous free tier that allows you to get going. 

**Daily Credit Limit:** 1, 000 Credits

| Type of request | Credit used |
| :--- | :--- |
| Static Read | 1 |
| Dynamic Read | 2 |
| Dynamic Update | 2 |
| Dynamic Delete | 2 |

## Pay as you go

We offer a pay as you go service. We do not automatically bill you, and instead you must top up your workspace with credits. You are therefore not limited by how many credits you can get, however each type of request will use a different amount of credits.

| Type of request | Credit used |
| :--- | :--- |
| Static Read | 1 |
| Dynamic Read | 2 |
| Dynamic Update | 2 |
| Dynamic Delete | 2 |

You can top up your account via Credit or Debit Card. **PayPal is not currently offered**.

