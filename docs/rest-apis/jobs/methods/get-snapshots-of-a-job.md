---
layout: default
parent: Jobs
title: Get Snapshots of a Job
permalink: /jobs/get-snapshots-of-a-job
nav_order: 3
---

## HTTP Request

```
GET {{ site.main_api_base_url }}/jobs/v1/snapshots/{client_job_id}
```
## Authorization

*Bearer Token*

Policy
[Job_ReadAll]({{site.url}}{{site.baseurl}}/authentication/policies#job_readall)

## Headers

| Key     | Value        |
| ----------- | ----------- |
| Authorization | Bearer {token}      |

## Path Parameters

| Parameter   | Type        |
| ----------- | ----------- |
| client_job_id | string      |

## Response Body
### JSON Representation
```


```
