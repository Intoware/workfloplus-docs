---
layout: default
parent: Workflows
title: Delete Workflow Version
permalink: /workflows/delete-workflow-version
nav_order: 10
---


## HTTP Request

```
DELETE {{ site.main_api_base_url }}/workflows/v2/{workflowId}/{workflowVersionId}
```


## Authorization
*Bearer Token*

Policy
[Workflow_Delete]({{site.url}}{{site.baseurl}}/authentication/policies#workflow_delete)



## Headers

| Key     | Value        |
| ----------- | ----------- |
| Authorization | Bearer {token}      |


## Path Parameters


| Parameter   | Type        |
| ----------- | ----------- |
| workflowId | string      |
| workflowVersionId | string      |