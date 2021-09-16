---
layout: default
parent: Users
title: Unlock User
permalink: /users/unlock-user
nav_order: 3
---


## HTTP Request

```
POST https://accounts.workfloplus.com/api/team/{user_id}/unlock
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
