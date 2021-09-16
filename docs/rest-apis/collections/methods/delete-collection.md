---
layout: default
parent: Collections
title: Delete Collection
permalink: /collections/delete-collection
nav_order: 5
---


## HTTP Request

```
DEL {{ site.main_api_base_url }}/collections/v1/collection/{collection_id}
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
| collection_id | string      |

