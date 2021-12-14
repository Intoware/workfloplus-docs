---
layout: default
parent: Trigger
title: Unarchive Trigger
permalink: /trigger/unarchive-trigger
nav_order: 6
---

## HTTP Request
```
PUT {{ site.main_api_base_url }}/trigger/v2/unarchive/{triggerId}
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

