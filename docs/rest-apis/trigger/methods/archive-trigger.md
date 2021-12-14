---
layout: default
parent: Trigger
title: Archive Trigger
permalink: /trigger/archive-trigger
nav_order: 5
---

## HTTP Request
```
DEL {{ site.main_api_base_url }}/trigger/v2/{triggerId}
```
## Authorization

*Bearer Token*

Policy
[Trigger_Admin]({{site.url}}{{site.baseurl}}/authentication/policies#trigger_admin)

## Headers

| Key     | Value        |
| ----------- | ----------- |
| Authorization | Bearer {token}      |

## Path Parameters

| Parameter   | Type        |
| ----------- | ----------- |
| triggerId        | string      |

