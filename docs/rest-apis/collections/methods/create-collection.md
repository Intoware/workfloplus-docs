---
layout: default
parent: Collections
title: Create Collection
permalink: /collections/create-collection
nav_order: 3
---


## HTTP Request

```
POST {{ site.main_api_base_url }}/collections/v1/collection
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

## Request Body
### JSON Representation
```
{
  "name":"New Collection"
}
```
## Response Body
### JSON Representation
```
{
  "collectionId":"61403c1230e5a30001d4440b"
}
```
