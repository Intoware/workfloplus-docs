---
layout: default
parent: Users
title: Get User Permissions
permalink: /users/get-user-permissions
nav_order: 3
---


## HTTP Request

```
GET https://accounts.workfloplus.com/api/team/user/{user_id}/permissions
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


## Response Body
### JSON Representation
```
{
  "dataViewer": true,
  "executor":true
}
```