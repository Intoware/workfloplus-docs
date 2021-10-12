---
layout: default
parent: Scheduler
title: Update the Status of a Scheduled Job
permalink: /scheduler/update-job-status
nav_order: 5
---

## HTTP Request
```
PUT {{ site.main_api_base_url }}/scheduledjobs/v1/{scheduled_job_id}/status
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

## Request Body
### JSON Representation
```
{
  "state":"Completed",
  "updated":"2021-10-06T07:24:52.44"
}

```
NB: A job can't be completed until all tasks in a job are completed.
