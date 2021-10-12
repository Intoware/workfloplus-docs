---
layout: default
parent: Report Templates
title: Update Template Metadata
permalink: /reporttemplates/update-template-metadata
nav_order: 8
---

## HTTP Request
```
PUT {{ site.main_api_base_url }}/reporttemplates/v1/metadata/{reportTemplate_id}
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

## Request Body
### JSON Representation
```
{  
    "key":"value"
}
```