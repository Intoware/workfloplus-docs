---
layout: default
parent: TeamSettings
title: Set TeamSettings to Defaults
permalink: /teamsettings/set-teamsettings-to-defaults
nav_order: 1
---


## HTTP Request

```
POST {{ site.main_api_base_url }}/teamsettings/v1/defaults
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

