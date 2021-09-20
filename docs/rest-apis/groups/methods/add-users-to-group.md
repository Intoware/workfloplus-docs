---
layout: default
parent: Groups
title: Add Users to Group 
permalink: /groups/add-users-to-group
nav_order: 6
---

## HTTP Request

```
PUT https://accounts.workfloplus.com/api/group/{group_id}/users
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
[
 "5dd501931da0b45001bf0da3",
 "5dd501931da0b30551bf0ra3"
]
```
User Ids of the users to be added are given in json body.