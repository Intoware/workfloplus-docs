---
layout: default
grand_parent: Collections
parent: Upload Collection
title: Create Collection Upload Session
permalink: /collections/upload-collection/create-collection-upload-session
nav_order: 1
---


## HTTP Request

```
POST https://accounts.workfloplus.com/collections/v1/upload
```

## Authorization

*Bearer Token*

Policy
[Workflow_Create]({{site.url}}{{site.baseurl}}/authentication/policies#workflow_create)

## Headers

| Key     | Value        |
| ----------- | ----------- |
| Authorization | Bearer {token}      |
| Content-Type | application/json      |

## Request Body
### JSON Representation
```
{
 "blockSize":102400,
 "fileSize":3134,
 "friendlyFileName":"ExampleCSV.csv",
 "collectionId":"61403c1230e5a30001d4440b"
}
```
## Response Body
### JSON Representation
```
{
  "id":"61404bfc60e5c32001d44625"
}
```
