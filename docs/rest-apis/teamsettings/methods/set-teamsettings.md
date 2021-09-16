---
layout: default
parent: TeamSettings
title: Set TeamSettings
permalink: /teamsettings/set-teamsettings
nav_order: 2
---


## HTTP Request

```
POST https://accounts.workfloplus.com/teamsettings/v1/
```


## Authorization

*Bearer Token*

Policy
[TeamSettings_Admin]({{site.url}}{{site.baseurl}}/authentication/policies#teamsettings_admin)


## Headers

| Key     | Value        |
| ----------- | ----------- |
| Authorization | Bearer {token}      |
| Content-Type | application/json      |

## Request Body
### JSON Representation
```
{
     "DisableJobRestart":true,
       "EnableJobNaming":false
}
```