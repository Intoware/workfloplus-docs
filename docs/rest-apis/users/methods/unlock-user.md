---
layout: default
parent: Users
title: Unlock User
permalink: /users/unlock-user
nav_order: 3
---


## HTTP Request

```
POST {{ site.accounts_api_base_url }}/team/{user_id}/unlock
```


## Authorization

*Bearer Token*

Policy
[Team_Admin]({{site.url}}{{site.baseurl}}/authentication/policies#team_admin)


## Headers

| Key     | Value        |
| ----------- | ----------- |
| Authorization | Bearer {token}      |

## Path Parameters


| Parameter   | Type        |
| ----------- | ----------- |
| user_id | string      |
