---
layout: default
parent: Users
title: Get User
permalink: /users/get-user
nav_order: 2
---


## HTTP Request

```
GET https://accounts.workfloplus.com/api/team/user/{user_id}
```


## Authorization

*Bearer Token*

Policy
Any Valid Token


## Headers

| Key     | Value        |
| ----------- | ----------- |
| Authorization | Bearer {token}      |


## Path Parameters


| Parameter   | Type        |
| ----------- | ----------- |
| userId | string      |


## Response Body
### JSON Representation
```
{
    "userId": "60df2148ad6cbd0001d86a1d",
    "username": "colin.pope@solarenergy.com",
    "emailAddress": "colin.pope@solarenergy.com",
    "name": "Colin Pope",
    "created": "2021-07-02T14:23:04.352Z",
    "locked": false
}
```