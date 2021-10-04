---
layout: default
parent: Jobs
title: Get Job by Job Id
permalink: /jobs/get-job-by-jobId
nav_order: 5
---

## HTTP Request

```
GET {{ site.main_api_base_url }}/jobs/v1/bson/{job_id}
```
## Authorization

*Bearer Token*

Policy
[Job_Read]({{site.url}}{{site.baseurl}}/authentication/policies#job_read)

## Headers

| Key     | Value        |
| ----------- | ----------- |
| Authorization | Bearer {token}      |

## Path Parameters

| Parameter   | Type        |
| ----------- | ----------- |
| job_id | string      |

## Response Body
### JSON Representation
```
[
  {
    "jobId":"5fa2a458980724000149rq40",
    "metadata":{
      "clientJobId":"8a07b1c0-56ba-433d-8a24-adddgb3e150c",
      "workflowId":"a454a699-173f-429e-b6cd-fefd92d0a1er",
      "workflowVersionId":"c683d13a-4cda-4683-1276-e7fcfb9c1c52",
      "jobTitle":"Example Workflow Job 1",
      "metadata":{
        "ScheduledJobId":"5fa2a3d17afcb9000179ad01",
        "ScheduledTaskId":"c95a93e0-b24f-44c3-a62f-7304c7ea7f2a"
      },
      "created":"2020-11-04T12:53:42.266Z",
      "updated":"2020-11-04T12:53:46.676Z",
      "modified":"2020-11-04T12:53:47Z",
      "status":"Paused",
      "userId":"5d8cac54860b8100016b1987",
      "currentStep":{
        "singleStep":{
          "values":[
          ],
          "valueResourceIds":[
          ],
          "uniqueStepId":"0ffad266-89e0-4659-936b-c0f92d043c81",
          "previousUniqueStepId":"",
          "userId":"5d8cac54860b8103316b1987",
          "userName":"api.user1@example.com",
          "deviceId":null,
          "stepId":"41443154-f511-478b-bcca-849440421061",
          "stepNumber":1,
          "stepTitle":"Enter Text",
          "stepDescription":"",
          "stepType":"Text",
          "connectionType":null,
          "started":"2020-11-04T12:53:42.687Z",
          "completed":null,
          "updated":"2020-11-04T12:53:46.664Z",
          "cancelled":null,
          "timeEvents":{
            "2020-11-04T12:53:46.664Z":0
          },
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
      },
      "abandonReason":null,
      "username":"api.user1@example.com",
      "workflowName":"Example Workflow"
    },
    "completedSteps":null,
    "cancelledSteps":null,
    "team":"apiteam",
    "hierarchyStack":null,
    "packetIds":null,
    "jobExclusion":[
    ],
    "excluded":false
  },
   {
    "jobId":"5f046ecf7df8a5000110cc54",
    "metadata":{
      "clientJobId":"f6ec68ae-a0b9-4725-aef4-9fb224be8e9d",
      "workflowId":"a454a699-173f-429e-b6cd-fefd92d0a1er",
      "workflowVersionId":"c683d13a-4cda-4683-1276-e7fcfb9c1c52",
      "jobTitle":"Example Workflow Job 2",
      "metadata":{
      },
      "created":"2020-07-07T12:47:09.281Z",
      "updated":"2020-07-07T12:47:17.619Z",
      "modified":"2020-07-07T12:47:17Z",
      "status":"Completed",
      "userId":"5d8cac54860b8103416b1987",
      "currentStep":null,
      "abandonReason":null,
      "username":"api.user2@example.com",
      "workflowName":"Example Workflow"
    },
    "completedSteps":null,
    "cancelledSteps":null,
    "team":"testteam",
    "hierarchyStack":null,
    "packetIds":null,
    "jobExclusion":[
    ],
    "excluded":false
  }
]

```
