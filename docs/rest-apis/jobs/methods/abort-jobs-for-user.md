---
layout: default
parent: Jobs
title: Abort Jobs for an User
permalink: /jobs/abort-jobs-for-user
nav_order: 13
---

## HTTP Request

```
PUT {{ site.main_api_base_url }}/jobs/v1/abort/?{user_id}
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
| user_id | string      |

NB: Only incomplete jobs can be aborted.
    When an User Id is not specified it would delete all users/team's incomplete jobs.
 

