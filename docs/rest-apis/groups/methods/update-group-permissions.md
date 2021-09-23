---
layout: default
parent: Groups
title: Update Group Permissions
permalink: /groups/Update-group-permissions
nav_order: 5
---

## HTTP Request

```
PUT https://accounts.workfloplus.com/api/group/{group_id}/permissions
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


## Request Body
### JSON Representation
```
{
"dataViewer":"true",
"editor":"true",
"modifier":"true",
"executor":"true",
"approver":"false"
}

```
