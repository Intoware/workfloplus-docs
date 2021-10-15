---
layout: default
parent: Report Templates
title: Delete Report Template
permalink: /reporttemplates/delete-report-template
nav_order: 5
---

## HTTP Request
```
DEL {{ site.main_api_base_url }}/reporttemplates/v1/{reportTemplate_id}
```
## Authorization

*Bearer Token*

Policy
[Reports_Create]({{site.url}}{{site.baseurl}}/authentication/policies#reports_create)

## Headers

| Key     | Value        |
| ----------- | ----------- |
| Authorization | Bearer {token}      |

## Path Parameters

| Parameter   | Type        |
| ----------- | ----------- |
| reportTemplate_id | string      |


