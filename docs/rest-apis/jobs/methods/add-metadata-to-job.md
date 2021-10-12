---
layout: default
parent: Jobs
title: Add Metadata to a Job
permalink: /jobs/add-metadata-to-job
nav_order: 11
---

## HTTP Request

```
POST {{ site.main_api_base_url }}/jobs/v1/{client_job_id}/metadata
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

## Request Body
### JSON Representation
```
{
    "key": "value"
}
```