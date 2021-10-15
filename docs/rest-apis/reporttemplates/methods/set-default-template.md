---
layout: default
parent: Report Templates
title: Set Default Report Template
permalink: /reporttemplates/set-default-template
nav_order: 6
---

## HTTP Request
```
PUT {{ site.main_api_base_url }}/reporttemplates/v1/default/{reportTemplate_id}
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
