---
layout: default
parent: Trigger
title: Update Trigger
permalink: /trigger/update-trigger
nav_order: 4
---

## HTTP Request
```
PUT {{ site.main_api_base_url }}/trigger/v2/{triggerId}
```
## Authorization

*Bearer Token*

Policy
[Trigger_Admin]({{site.url}}{{site.baseurl}}/authentication/policies#trigger_admin)

## Headers

| Key     | Value        |
| ----------- | ----------- |
| Authorization | Bearer {token}      |

## Path Parameters

| Parameter   | Type        |
| ----------- | ----------- |
| triggerId        | string      |

## Request Body
### JSON Representation
```
{
    "name":"APi Trigger Ex 1",
    "description":"Updating trigger description via api call",
    "templateTags":[],
    "objectIds":[],
    "templateIds":[],
    "triggerType":"Email",
    "triggerOptions":{"recipients":"","sendCopyToUser":"true"},
    "pdfRequirement":"NotRequired",
    "reportTemplateId":null,
    "disabled":true
}
```
