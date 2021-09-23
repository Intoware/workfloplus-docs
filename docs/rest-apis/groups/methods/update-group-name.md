---
layout: default
parent: Groups
title: Update Group Name
permalink: /groups/Update-group-name
nav_order: 4
---

## HTTP Request

```
PUT {{ site.accounts_api_base_url }}/group/{group_id}
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
| group_id | string      |


## Request Body
### JSON Representation
```
{
  "name":"New Group Name"
}
```

## Response Body
### JSON Representation
```
{
  "id":"5e4a95c36abe6e0001f80592",
  "name":"New Group Name"
}
```
