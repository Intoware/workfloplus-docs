---
layout: default
parent: Users
title: Update User Details
permalink: /users/update-user-details
nav_order: 4
---


## HTTP Request

```
PUT {{ site.accounts_api_base_url }}/team/user/{user_id}
```


## Authorization

*Bearer Token*

Policy
[Team_Admin]({{site.url}}{{site.baseurl}}/authentication/policies#team_admin)


## Headers

| Key     | Value        |
| ----------- | ----------- |
| Authorization | Bearer {token}      |
| Content-Type | application/json      |


## Path Parameters


| Parameter   | Type        |
| ----------- | ----------- |
| user_id | string      |


## Request Body
### JSON Representation
```
{
    "Name": "Chege Naengop"
}
```

