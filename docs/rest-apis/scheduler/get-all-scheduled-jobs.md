---
layout: default
parent: Scheduler
title: Get All Scheduled Jobs
permalink: /jobs/get-all-scheduled-jobs
nav_order: 1
---

## HTTP Request
```
GET {{ site.main_api_base_url }}/scheduledjobs/v1
```
## Authorization

*Bearer Token*

Policy
[Schedule_ReadAll]({{site.url}}{{site.baseurl}}/authentication/policies#schedule_readall)

## Headers

| Key     | Value        |
| ----------- | ----------- |
| Authorization | Bearer {token}      |

## Response Body
### JSON Representation
```
[
  {
    "jobId":"5f365519a2ed5a2301f2d303",
    "created":"2021-08-14T09:10:49.636Z",
    "updated":"2021-08-14T09:10:49.636Z",
    "state":"Scheduled",
    "name":"Scheduled Job1",
    "description":"Scheduled Job1 - WF1",
    "priority":false,
    "dueByDate":null,
    "assignedUserIds":[
    ],
    "tasks":
    [
      {
        "taskType":"Workflow",
        "taskId":"707c5cb6-8171-4232-baca-f7c94dc42ea9",
        "artifactId":null,
        "jobId":null,
        "clientJobId":null,
        "updated":null,
        "modified":null,
        "state":0
      }
    ]
  },
  {
    "jobId":"601170d37e97f340011ca1e3",
    "created":"2021-01-27T13:55:31.045Z",
    "updated":"2021-01-27T13:58:13.452Z",
    "state":"Completed",
    "name":"Scheduled Job2",
    "description":"Scheduled Job1 - WF2",
    "priority":true,
    "dueByDate":"2021-01-27T15:30:00Z",
    "assignedUserIds":[
      "5d8cacd378111f0001e71db0"],
    "tasks":
    [
      {
        "taskType":"Workflow",
        "taskId":"610d8443-fdac-443c-bca5-52c761a56561",
        "artifactId":"012ee471-9954-4b53-93ac-1062e43bffa3",
        "jobId":"6011713d19863200010ed4b5",
        "clientJobId":"7aa2546f-be00-45fd-94fa-d3ccfbe22fdb",
        "updated":"2021-01-27T13:58:13.363Z",
        "modified":"2021-01-27T13:58:13.366Z",
        "state":3
      }
    ]
  }
]
  
```

