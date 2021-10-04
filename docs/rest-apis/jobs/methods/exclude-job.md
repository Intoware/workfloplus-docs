---
layout: default
parent: Jobs
title: Exclude a Job
permalink: /jobs/exclude-job
nav_order: 10
---

## HTTP Request

```
PUT {{ site.main_api_base_url }}/jobs/v1/{client_job_id}
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

## Request Body
### JSON Representation
```
{
    "userId": "5d8cac54860b8103316b1987",
    "reason": "Api Exclude Job Test",
    "isExcluded": "true"
}
```