---
layout: default
parent: Jobs
title: Create Job
permalink: /jobs/create-job
nav_order: 12
---

## HTTP Request

```
POST {{ site.main_api_base_url }}/jobs/v1
```
## Authorization

*Bearer Token*

Policy
[Workflow_Execute]({{site.url}}{{site.baseurl}}/authentication/policies#workflow_execute)

## Headers

| Key     | Value        |
| ----------- | ----------- |
| Authorization | Bearer {token}      |

## Request Body
### JSON Representation
```
{
  "metadata":{
    "clientJobId":"cb3dc8dc-4162-47c4-af05-3575034f99e5",
    "workflowId":"b62f2507-b4e7-4248-83d3-29c03a158fbe",
    "workflowVersionId":"2831f333-af02-4d89-875d-0bceadeb16ed",
    "jobTitle":"Api Test 2",
    "metadata":{
      "Key1":"V1",
    },
    "created":"2021-10-01T12:48:12.215Z",
    "updated":"2021-10-01T12:48:13.824Z",
    "modified":"2021-10-01T12:48:14Z",
    "status":"Completed",
    "userId":"5d8cac54860b8103316b1987",
    "currentStep":null,
    "abandonReason":null,
    "username":"api.user1@example.com",
    "workflowName":"Example Workflow"
  },
  "completedSteps":[
    {
      "singleStep":{
        "values":[
        ],
        "valueResourceIds":[
        ],
        "uniqueStepId":"c025f569-8148-4a75-a2e8-a9bc19da911d",
        "previousUniqueStepId":"",
        "userId":"5d8cac54860b8103316b1987",
        "userName":"api.user1@example.com",
        "deviceId":null,
        "stepId":"ec7eee0d-5115-4141-847a-64c28694dde2",
        "stepNumber":1,
        "stepTitle":"Instruction",
        "stepDescription":"",
        "stepType":"ConfirmStep",
        "connectionType":null,
        "started":"2021-10-01T12:48:12.265Z",
        "completed":"2021-10-01T12:48:13.8Z",
        "updated":"2021-10-01T12:48:13.8Z",
        "cancelled":null,
        "timeEvents":null,
        "note":null,
        "noteResourceFilenames":null,
        "coordinates":null,
        "parentStepId":null,
        "parentUniqueStepId":null,
        "parentStepTitle":null,
        "parentStepDescription":null,
        "metadata":{
          "tags":""
        }
      },
      "reportStep":null
    }],
  "cancelledSteps":null,
  "team":"apiteam",
  "hierarchyStack":null,
  "packetIds":null,
  "jobExclusion":[
  ],
  "excluded":false
}
```
## Response Body
### JSON Representation
```
{
  "jobId":"615704cbb249fb12315fcfbc",
  "metadata":{
    "clientJobId":"cb3dc8dc-4162-47c4-af05-3575034f99e5",
    "workflowId":"b62f2507-b4e7-4248-83d3-29c03a158fbe",
    "workflowVersionId":"2831f333-af02-4d89-875d-0bceadeb16ed",
    "jobTitle":"Api Test 2",
    "metadata":{
      "Key1":"V1",
    },
    "created":"2021-10-01T12:48:12.215Z",
    "updated":"2021-10-01T12:48:13.824Z",
    "modified":"2021-10-01T12:48:14Z",
    "status":"Completed",
    "userId":"5d8cac54860b8103316b1987",
    "currentStep":null,
    "abandonReason":null,
    "username":"api.user1@example.com",
    "workflowName":"Example Workflow"
  },
  "completedSteps":[
    {
      "singleStep":{
        "values":[
        ],
        "valueResourceIds":[
        ],
        "uniqueStepId":"c025f569-8148-4a75-a2e8-a9bc19da911d",
        "previousUniqueStepId":"",
        "userId":"5d8cac54860b8103316b1987",
        "userName":"api.user1@example.com",
        "deviceId":null,
        "stepId":"ec7eee0d-5115-4141-847a-64c28694dde2",
        "stepNumber":1,
        "stepTitle":"Instruction",
        "stepDescription":"",
        "stepType":"ConfirmStep",
        "connectionType":null,
        "started":"2021-10-01T12:48:12.265Z",
        "completed":"2021-10-01T12:48:13.8Z",
        "updated":"2021-10-01T12:48:13.8Z",
        "cancelled":null,
        "timeEvents":null,
        "note":null,
        "noteResourceFilenames":null,
        "coordinates":null,
        "parentStepId":null,
        "parentUniqueStepId":null,
        "parentStepTitle":null,
        "parentStepDescription":null,
        "metadata":{
          "tags":""
        }
      },
      "reportStep":null
    }],
  "cancelledSteps":null,
  "team":"apiteam",
  "hierarchyStack":null,
  "packetIds":null,
  "jobExclusion":[
  ],
  "excluded":false
}
```