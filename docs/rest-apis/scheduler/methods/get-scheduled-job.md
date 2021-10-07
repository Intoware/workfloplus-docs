---
layout: default
parent: Scheduler
title: Get Scheduled Job
permalink: /jobs/get-scheduled-job
nav_order: 2
---

## HTTP Request
```
GET {{ site.main_api_base_url }}/scheduledjobs/v1/{scheduled_job_id}
```
## Authorization

*Bearer Token*

Policy
[Schedule_Read]({{site.url}}{{site.baseurl}}/authentication/policies#schedule_read)

## Headers

| Key     | Value        |
| ----------- | ----------- |
| Authorization | Bearer {token}      |

## Path Parameters

| Parameter   | Type        |
| ----------- | ----------- |
| scheduled_job_id | string      |

## Response Body
### JSON Representation
```
{
  "jobId":"615c2057c5722f000168e37f",
  "created":"2021-10-05T09:52:23.341Z",
  "updated":"2021-10-05T09:52:23.341Z",
  "state":"Scheduled",
  "name":"API Scheduler Example Job 1",
  "description":"To Demo Scheduler Apis",
  "priority":true,
  "dueByDate":"2021-10-05T22:59:00Z",
  "assignedUserIds":[
    "5d8cac54860b81ee016b1987"],
  "tasks":[
    {
      "taskType":"Workflow",
      "taskId":"d7020dd1-8ce9-42ce-90f2-8d2f7f734c20",
      "artifactId":"b62f2507-b4e7-4248-83d3-29c03b158fbe",
      "jobId":null,
      "clientJobId":null,
      "updated":null,
      "modified":null,
      "state":0
    }]
}
```
NB:
Task State

1. 1 - Active 
2. 2 - Paused 
3. 3 - Completed  
4. 4 - Abandoned  
5. 0 - Not started 


