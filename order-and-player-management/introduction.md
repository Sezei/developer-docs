---
description: >-
  A brief introduction to the Hyra Order and Player Management API and Datastore
  service
---

# Introduction

{% hint style="info" %}
This API is still in **Alpha**. You must be invited to use this API. 
{% endhint %}

Hyra runs an order and point management system for groups requiring an external system and API to manage points. 

{% tabs %}
{% tab title="Player Management" %}
Storing users data externally outside of your game has many benefits. With Hyra's Player Management, you can access this system outside of your game, and we'll manage the authentication, logging and the interface. You can use this to store points and play history.

## Why would I use this?

This API is designed for a **replacement** to datastores. Hyra will store the points externally and keep track of all points for you. 

These points are stored in Hyra's database, which is managed in a protected environment. Hyra will take of:

* Systems backups
* Uptime management
* Token management
* Log management
* Hosting and redundancy

You can see the exact history on a timeline of how a user gained their points, so you can ensure nobody is cheating points or claiming they are missing points. 

#### Redundancy

Hyra's API Database used in V2.0 is a multi-cluster highly redundant database hosted with geo redundancy to ensure it is always online.

#### Worry free datastore

Hyra understands the complexity of managing an external database. Leave the complexity and administration to Hyra. We'll handle everything from backups to updates to ensure that your data is secure and redundant.

#### Highly Scalable

Scale to support your group's growth. From 10 players to 1000's, Hyra's managed data solution can scale to meet your needs.

#### Backups

Hyra keeps copies of all of its data for 7 days. We carry out daily backups of our database, which we can roll back to in the event of a disaster.

#### Automatic failover

In the event of a failure, our managed data solution will automatically elect a new primary replica to take over. Hyra has pools of standby nodes to minimize downtime. 

#### Security you can trust

With our API Token security, you can trust that your data is protected. With our IP tables and whitelist management, you can only allow access from certain machines. Data is also encrypted in transit.
{% endtab %}

{% tab title="Order Management" %}
Throw away that horrible Discord webhook and switch to Hyra Order Management. 

* Search users by usernames and find exactly which items they gave, what time they gave them and who they gave them to.
* Identify cheaters by seeing all of the context. 

Hyra's order management is a realtime way of monitoring your orders both within and outside of your game, giving your moderators and medium ranks a central space of history and employee logs.
{% endtab %}
{% endtabs %}

Hyra's Point Management and Order Management and point systems can be accessed through both **raw REST Http Requests** and the **HyraAPIModule**

