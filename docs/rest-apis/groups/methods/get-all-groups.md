---
layout: default
parent: Groups
title: Get All Groups
permalink: /groups/get-all-groups
nav_order: 1
---

## HTTP Request

```
GET {{ site.accounts_api_base_url }}/group
```
## Authorization

*Bearer Token*

Policy
Any Valid Token

## Headers

| Key     | Value        |
| ----------- | ----------- |
| Authorization | Bearer {token}      |

## Response Body
### JSON Representation
```
[
  {
    "id":"5e4a95c36abe6e0001f80592",
    "name":"Example Group 1"
  },
  {
    "id":"5f367fe76147f40001def972",
    "name":"Example Group 2"
  }
]

```
