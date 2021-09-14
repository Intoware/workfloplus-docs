---
layout: default
parent: Users
title: Create User
permalink: /users/create-user
nav_order: 3
---


## HTTP Request

```
POST https://accounts.workfloplus.com/api/team/user
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


## Request Body
### JSON Representation
```
{
    "username": "chege.naengop@solarenergy.com",
    "emailAddress": "chege.naengop@solarenergy.com",
    "name": "Chege Naengop"
}
```


## Response Body
### JSON Representation
```
{
    "password": "3DfJ/84dY",
    "teamName": "solarenergy",
    "mode": 0,
    "userId": "60e3054c04cb64000128d658",
    "username": "chege.naengop@solarenergy.com",
    "emailAddress": "chege.naengop@solarenergy.com",
    "name": "Chege Naengop",
    "created": "2021-07-05T13:12:44.7442233Z",
    "locked": false
}
```