---
layout: default
parent: Scheduler
title: Create a Scheduled Job
permalink: /scheduler/create-scheduled-job
nav_order: 8
---

## HTTP Request
```
POST {{ site.main_api_base_url }}/scheduledjobs/v1
```
## Authorization

*Bearer Token*

Policy
[Schedule_Admin]({{site.url}}{{site.baseurl}}/authentication/policies#schedule_admin)

## Headers

| Key     | Value        |
| ----------- | ----------- |
| Authorization | Bearer {token}      |

## Request Body
### JSON Representation
```
{
  "name":"API Scheduler Example Job 1",
  "description":"To Demo Scheduler Apis",
  "tasks":
  [
      {
       "taskType":"workflow","
       "artifactId":"b62f2507-b4e7-4248-83d3-29c03a158fae"
      }
  ],
  "assignedUserIds":["5d91f997ccfe6a0001dc9dc1"],
  "dueByDate":null,
  "priority":false
}
```
## Response Body
### JSON Representation
```
{
  "jobId":"615da9233ed8fe0021364451",
  "created":"2021-10-06T13:48:19.342407Z",
  "updated":"2021-10-06T13:48:19.342407Z",
  "state":"Scheduled",
  "name":"API Scheduler Example Job 1",
  "description":"To Demo Scheduler Apis",
  "priority":false,
  "dueByDate":null,
  "assignedUserIds":[
    "5d8cac54860b8100016b1987"],
  "tasks":[
    {
      "taskType":"Workflow",
      "taskId":"dbd38dd1-fc76-4a3a-8e4c-27a1e9a4148c",
      "artifactId":"b62f2507-b4e7-4218-83d3-29c03a158fae",
      "jobId":null,
      "clientJobId":null,
      "updated":null,
      "modified":null,
      "state":0
    }]
}
```
NB:
artifactId is the workflowId.