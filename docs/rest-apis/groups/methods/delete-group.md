---
layout: default
parent: Groups
title: Delete Group 
permalink: /groups/delete-group
nav_order: 8
---

## HTTP Request

```
DEL {{ site.accounts_api_base_url }}/group/{group_id}
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
| group_id | string      |
