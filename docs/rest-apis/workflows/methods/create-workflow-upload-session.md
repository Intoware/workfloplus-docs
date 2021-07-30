---
layout: default
grand_parent: Workflows
parent: Upload a Workflow
title: Create Workflow Upload Session
permalink: /workflows/upload/create-workflow-upload-session
nav_order: 1
---


## HTTP Request

```
POST {{ site.main_api_base_url }}/workflows/v2/upload
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
    "blockSize": {BLOCKSIZE},
    "fileSize": {FILESIZE},
    "friendlyFileName": "Workflow1.zip"
}
```


## Response Body
### JSON Representation
```
{
    "id": "60578b426a9eb4000114ec13"
}
```