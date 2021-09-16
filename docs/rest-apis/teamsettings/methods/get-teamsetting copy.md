---
layout: default
parent: TeamSettings
title: Get TeamSetting
permalink: /teamsettings/get-teamsetting
nav_order: 3
---


## HTTP Request

```
GET {{ site.main_api_base_url }}/teamsettings/v1/{setting_key}
```


## Authorization

*Bearer Token*

Policy
[TeamSettings_Read]({{site.url}}{{site.baseurl}}/authentication/policies#teamsettings_read)


## Headers

| Key     | Value        |
| ----------- | ----------- |
| Authorization | Bearer {token}      |

## Path Parameters


| Parameter   | Type        |
| ----------- | ----------- |
| setting_key (DisableJobRestart) | string      |


## Response Body
### JSON Representation
```
{
  true
}
```
