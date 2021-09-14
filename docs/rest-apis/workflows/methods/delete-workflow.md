---
layout: default
parent: Workflows
title: Delete Workflow
permalink: /workflows/delete-workflow
nav_order: 11
---


## HTTP Request

```
DELETE {{ site.main_api_base_url }}/workflows/v2/{workflowId}
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