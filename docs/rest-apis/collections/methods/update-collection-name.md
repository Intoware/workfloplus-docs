---
layout: default
parent: Collections
title: Update Collection Name
permalink: /collections/update-collection-name
nav_order: 2
---


## HTTP Request

```
PUT https://accounts.workfloplus.com/collections/v1/collection/{collection_id}
```

## Authorization

*Bearer Token*

Policy
Any Valid Token

## Headers

| Key     | Value        |
| ----------- | ----------- |
| Authorization | Bearer {token}      |
| Content-Type | application/json      |

## Path Parameters


| Parameter   | Type        |
| ----------- | ----------- |
| collection_id | string      |

## Request Body
### JSON Representation
```
{
  "name":"New Collection Name"
}
```
