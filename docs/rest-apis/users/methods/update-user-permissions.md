---
layout: default
parent: Users
title: Update User Permissions
permalink: /users/update-user-permissions
nav_order: 4
---


## HTTP Request

```
PUT https://accounts.workfloplus.com/api/team/user/{userId}/permissions
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
| userId | string      |


## Headers


| Key     | Value        |
| ----------- | ----------- |
| Content-Type | application/json      |


## Request Body
### JSON Representation
```
{
    "admin": False,
    "dataViewer": True,
    "executor": True
}
```

