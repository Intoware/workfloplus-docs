---
layout: default
parent: Groups
title: Create Group 
permalink: /groups/create-group
nav_order: 2
---

## HTTP Request

```
POST {{ site.accounts_api_base_url }}/group
```
## Authorization

*Bearer Token*

Policy
[Team_Admin]({{site.url}}{{site.baseurl}}/authentication/policies#team_admin)

## Headers

| Key     | Value        |
| ----------- | ----------- |
| Authorization | Bearer {token}      |

## Request Body
### JSON Representation
```
{
  "name":"Group Name"
}
```

## Response Body
### JSON Representation
```
{
  "id":"5e4a95c36abe6e0001f80592",
  "name":"Group Name"
}
```