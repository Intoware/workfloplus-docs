---
layout: default
parent: Trigger
title: Get all Triggers
permalink: /trigger/get-all-triggers
nav_order: 1
---

## HTTP Request
```
GET {{ site.main_api_base_url }}/trigger/v2
```
## Authorization

*Bearer Token*

Policy
[Trigger_Read]({{site.url}}{{site.baseurl}}/authentication/policies#trigger_read)

## Headers

| Key     | Value        |
| ----------- | ----------- |
| Authorization | Bearer {token}      |

## Response Body
### JSON Representation
```
[
    {
        "triggerId": "61644119f2efe60001085778",
        "created": "2021-10-11T13:50:17Z",
        "updated": "2021-12-10T14:02:26Z",
        "name": "Trigger Api Ex 1",
        "description": null,
        "templateTags": [],
        "objectIds": [],
        "templateIds": [
            "a454a699-173f-429e-b3cd-fefd82d0a1e4"
        ],
        "triggerType": "Email",
        "triggerOptions": {
            "recipients": "",
            "sendCopyToUser": "true"
        },
        "reportTemplateId": "6163da95736e3c00014f9bee",
        "pdfRequirement": "FullImages",
        "disabled": false,
        "archived": false
    },
    {
        "triggerId": "5f02e48325b6dc00018b81e8",
        "created": "2020-07-06T08:44:51Z",
        "updated": "2020-07-06T08:44:51Z",
        "name": "Trigger Api Ex 2",
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
]

```
