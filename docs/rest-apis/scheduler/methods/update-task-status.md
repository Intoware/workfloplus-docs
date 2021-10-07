---
layout: default
parent: Scheduler
title: Update the Status of a Task in a Scheduled Job
permalink: /jobs/update-task-status
nav_order: 4
---

## HTTP Request
```
PUT {{ site.main_api_base_url }}/scheduledjobs/v1/{scheduled_job_id}/tasks/{task_id}/status
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
| task_id | string      |

## Request Body
### JSON Representation
```
{
  "clientJobId":"c0bda7f7-0a1f-400c-8276-cef1c4ae75ea",
  "state":"Paused",
  "updated":"2021-10-06T07:24:52.44"
}

```

