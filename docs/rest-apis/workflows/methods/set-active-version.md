---
layout: default
parent: Workflows
title: Set Active Version
permalink: /workflows/set-active-version
nav_order: 9
---


## HTTP Request

```
POST {{ site.main_api_base_url }}/workflows/v2/{workflowVersionId}/activate
```


## Authorization

*Bearer Token*

Policy
[Workflow_Modify]({{site.url}}{{site.baseurl}}/authentication/policies#workflow_modify)


## Headers

| Key     | Value        |
| ----------- | ----------- |
| Authorization | Bearer {token}      |


## Path Parameters


| Parameter   | Type        |
| ----------- | ----------- |
| workflowVersionId | string      |

