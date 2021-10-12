---
layout: default
parent: Report Templates
title: Get Report Template Names
permalink: /reporttemplates/get-template-names
nav_order: 3
---

## HTTP Request
```
GET {{ site.main_api_base_url }}/reporttemplates/v1/names
```
## Authorization

*Bearer Token*

Policy
[Reports_Create]({{site.url}}{{site.baseurl}}/authentication/policies#reports_create)

## Headers

| Key     | Value        |
| ----------- | ----------- |
| Authorization | Bearer {token}      |

## Response Body
### JSON Representation
```
[
  {
    "reportTemplateId":"5ec4f0fde9efaa00011a07bc",
    "name":"Report Template Example 1",
    "description":null,
    "templateVersions":null,
    "teamName":null,
    "lastUpdated":"0001-01-01T00:00:00",
    "template":null,
    "options":null,
    "isArchived":false,
    "metadata":{}
  },
  {
    "reportTemplateId":"5f036028e031440001c9a073",
    "name":"Report Template Example 2",
    "description":null,
    "templateVersions":null,
    "teamName":null,
    "lastUpdated":"0001-01-01T00:00:00",
    "template":null,
    "options":null,
    "isArchived":false,
    "metadata":{}
  }
]
```

