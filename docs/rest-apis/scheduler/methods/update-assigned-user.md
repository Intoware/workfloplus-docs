---
layout: default
parent: Scheduler
title: Update Assigned User for a Job
permalink: /scheduler/update-assigned-user
nav_order: 6
---

## HTTP Request
```
PUT {{ site.main_api_base_url }}/scheduledjobs/v1/{scheduled_job_id}/assignedUsers
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

## Request Body
### JSON Representation
```
{
  "assignedUserIds":["5d91f997ccfe6a0001dc9dc1"]
}

```
