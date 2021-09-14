---
layout: default
parent: Workflows
title: Update Workflow Metadata
permalink: /workflows/update-workflow-metadata
nav_order: 3
---


## HTTP Request

```
PUT {{ site.main_api_base_url }}/workflows/v2/{workflowId}
```


## Authorization

*Bearer Token*

Policy
[Workflow_Modify]({{site.url}}{{site.baseurl}}/authentication/policies#workflow_modify)


## Headers

| Key     | Value        |
| ----------- | ----------- |
| Authorization | Bearer {token}      |
| Content-Type | application/json      |


## Path Parameters


| Parameter   | Type        |
| ----------- | ----------- |
| workflowId | string      |


## Request Body
### JSON Representation
```
{
    "name": "Panel Repair Workflow - AP-6 Type",
    "description": "Ensure this workflow is used on the latest AP-6 type panels",
    "tags": ["Panel", "Repair", "AP-6"],
    liveObjectIds: ["5e4172bc9a21690001f361f1", "5e46a021785ccf0001e9a2f6"]
}
```


N.B. By default workflows are availble for use for any user with the required permissions, however it is possible to restrict the usage of workflow to specified individual users or user groups.
The *liveObjectIds* parameter is used to specify the users or groups; for a user include the *userId* and for a group include the *groupId*.