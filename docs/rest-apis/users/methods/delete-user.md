---
layout: default
parent: Users
title: Delete User
permalink: /users/delete-user
nav_order: 5
---


## HTTP Request

```
DEL {{ site.accounts_api_base_url }}/team/user/{user_id}
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