---
layout: default
parent: Jobs
title: Update a Job
permalink: /jobs/update-job
nav_order: 15
---

## HTTP Request

```
POST {{ site.main_api_base_url }}/jobs/v1/{client_job_id}
```
## Authorization

*Bearer Token*

Policy
[Job_Modify]({{site.url}}{{site.baseurl}}/authentication/policies#job_modify)

## Headers

| Key     | Value        |
| ----------- | ----------- |
| Authorization | Bearer {token}      |

## Path Parameters

| Parameter   | Type        |
| ----------- | ----------- |
| client_job_id | string      |

## Request Body
### JSON Representation
```
{
  "metadata":{
    "clientJobId":"cb3dc8dc-4162-47c4-af05-3575034f99e5",
    "workflowId":"b62f2507-b4e7-4248-83d3-29c03a158fbe",
    "workflowVersionId":"2831f333-af02-4d89-875d-0bceadeb16ed",
    "jobTitle":"Api Test 2 - Updated name",
    "metadata":{
      "Key1":"V1",
    },
    "created":"2021-10-01T12:48:12.215Z",
    "updated":"2021-10-01T12:48:13.824Z",
    "modified":"2021-10-01T12:48:14Z",
    "status":"Paused",
    "userId":"5d8cac54860b8103316b1987",
    "currentStep":null,
    "abandonReason":null,
    "username":"api.user1@example.com",
    "workflowName":"Example Workflow"
  },
}
```