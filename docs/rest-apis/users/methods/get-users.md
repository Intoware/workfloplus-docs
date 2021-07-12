---
layout: default
parent: Users
title: Get Users
permalink: /users/get-users
nav_order: 1
---


## HTTP Request

```
GET https://accounts.workfloplus.com/api/team/user
```


## Authorization
*Bearer Token*

Policy
Any Valid Token


## Headers

| Key     | Value        |
| ----------- | ----------- |
| Authorization | Bearer {token}      |


## Response Body
### JSON Representation
```
[
    {
        "userId": "60df2148ad6cbd0001d86a1d",
        "username": "colin.pope@solarenergy.com",
        "emailAddress": "colin.pope@solarenergy.com",
        "name": "Colin Pope",
        "created": "2021-07-02T14:23:04.352Z",
        "locked": false
    },
    {
        "userId": "60df09e19108b2e627754f54",
        "username": "talika.divan@solarenergy.com",
        "emailAddress": "talika.divan@solarenergy.com",
        "name": "Talika Divan busfield",
        "created": "2021-06-01T15:14:52.000Z",
        "locked": false
    }
]
```