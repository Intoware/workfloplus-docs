---
layout: default
parent: Jobs
title: Assign User to a Job
permalink: /jobs/assign-user
nav_order: 9
---

## HTTP Request

```
POST {{ site.main_api_base_url }}/jobs/v1/{client_job_id}/assign/{user_id}
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
| client_job_id | string      |
| user_id | string      |

NB: Aborted and Completed jobs can't be assigned to another user.

