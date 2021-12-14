---
layout: default
parent: Trigger
title: Create Trigger
permalink: /trigger/create-trigger
nav_order: 3
---

## HTTP Request
```
POST {{ site.main_api_base_url }}/trigger/v2
```
## Authorization

*Bearer Token*

Policy
[Trigger_Admin]({{site.url}}{{site.baseurl}}/authentication/policies#trigger_admin)

## Headers

| Key     | Value        |
| ----------- | ----------- |
| Authorization | Bearer {token}      |

## Request Body
### JSON Representation
```
{
    "disabled":true,
    "name":"API Trigger Ex 1",
    "triggerType":"Email"
}
```
## Response Body
### JSON Representation
```
{
    "triggerId": "61b70762ccc3a70q011c0462",
    "created": "2021-12-13T08:42:10Z",
    "updated": "2021-12-13T08:42:10Z",
    "name": "API Trigger Ex 2",
    "description": null,
    "templateTags": [],
    "objectIds": [],
    "templateIds": [],
    "triggerType": "Email",
    "triggerOptions": {},
    "reportTemplateId": null,
    "pdfRequirement": "NotRequired",
    "disabled": true,
    "archived": false
}
```
