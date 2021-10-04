---
layout: default
parent: Jobs
title: Abort a Job
permalink: /jobs/abort-job
nav_order: 7
---

## HTTP Request

```
POST {{ site.main_api_base_url }}/jobs/v1/{client_job_id}/abort
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

NB: Only incomplete jobs can be aborted.

