---
layout: default
parent: Users
title: Reset User's Password
permalink: /users/reset-user-password
nav_order: 3
---


## HTTP Request

```
POST https://accounts.workfloplus.com/api/team/{user_id}/resetpassword
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

  "password":"3DfJ/84dY"
}
```