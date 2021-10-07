---
layout: default
parent: Scheduler
title: Delete a Scheduled Job
permalink: /jobs/delete-scheduled-job
nav_order: 7
---

## HTTP Request
```
DEL {{ site.main_api_base_url }}/scheduledjobs/v1/{scheduled_job_id}
```
## Authorization

*Bearer Token*

Policy
[Schedule_Admin]({{site.url}}{{site.baseurl}}/authentication/policies#schedule_admin)

## Headers

| Key     | Value        |
| ----------- | ----------- |
| Authorization | Bearer {token}      |

## Path Parameters

| Parameter   | Type        |
| ----------- | ----------- |
| scheduled_job_id | string      |

