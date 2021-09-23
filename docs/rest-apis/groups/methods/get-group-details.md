---
layout: default
parent: Groups
title: Get Group Details
permalink: /groups/get-group-details
nav_order: 3
---

## HTTP Request

```
GET {{ site.accounts_api_base_url }}/group/{group_id}
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


## Response Body
### JSON Representation
```
{
  "groupId":"5e4a95c36abe6e0001f80592",
  "teamName":"Example Team",
  "name":"Example Group 1",
  "lowercaseName":"example group 1",
  "created":"2020-03-02T11:08:30Z",
  "users":[
    "5d8cab89860b81efr16b196a",
    "5d91f997ccfe6acf01dc9dc1"],
  "permissions":{
    "dataViewer":true,
    "editor":true,
    "modifier":true
  }
}

```
