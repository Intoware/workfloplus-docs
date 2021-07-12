---
layout: default
grand_parent: Workflows
parent: Upload a Workflow
title: Finalise Workflow Upload
permalink: /workflows/upload/finalise-workflow-upload
nav_order: 3
---


## HTTP Request

```
POST https://gateway.workfloplus.com/workflows/v2
```

## Authorization

*Bearer Token*

Policy
[Workflow_Create]({{site.url}}{{site.baseurl}}/authentication/policies#workflow_create)

## Headers

| Key     | Value        |
| ----------- | ----------- |
| Authorization | Bearer {token}      |


## Request Body
### JSON Representation
```
{
    "uploadId": "60578b426a9eb4000114ec13",
    "name": "Repair Process",
    "description": "Repair Process for all new and current Plant Machinery",
    "tags": ["Repairs", "Level 1 Process"],
    "versionNotes": "First version of the process"
}
```


## Response Body
### JSON Representation
```
{
    "workflowId": "4dcb1a1b-782f-4167-8a87-ca6b31ae877d"
}
```