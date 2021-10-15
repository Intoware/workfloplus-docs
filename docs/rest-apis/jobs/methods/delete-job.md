---
layout: default
parent: Jobs
title: Delete a Job
permalink: /jobs/delete-job
nav_order: 8
---

## HTTP Request

```
DEL {{ site.main_api_base_url }}/jobs/v1/{client_job_id}
```
## Authorization

*Bearer Token*

Policy
[Job_Modify]({{site.url}}{{site.baseurl}}/authentication/policies#job_modify)

## Headers 

| Key     | Value        |
| ----------- | ----------- |
| Authorization | Bearer {token}      |

## Path Parameters

| Parameter   | Type        |
| ----------- | ----------- |
| client_job_id | string      |


