---
layout: default
parent: Workflows
title: Get Workflows
permalink: /workflows/get-workflows
nav_order: 1
---


## HTTP Request

```
GET {{ site.main_api_base_url }}/workflows/v2
```


## Authorization
*Bearer Token*

Policy
[Workflow_Read]({{site.url}}{{site.baseurl}}/authentication/policies#workflow_read)



## Headers

| Key     | Value        |
| ----------- | ----------- |
| Authorization | Bearer {token}      |


## Response Body
### JSON Representation
```
[
    {
        "workflowId": "75b81832-257b-4a7a-9e05-g121acc11a67",
        "created": "2020-01-14T11:53:47Z",
        "lastUpdated": "2020-02-04T08:18:49Z",
        "teamName": "solarenergy",
        "activeVersionId": "873b6fc9-6e62-4d8f-aac5-42c3aa8235a8",
        "name": "Panel Repair Workflow",
        "description": "",
        "isArchived": false,
        "liveObjectIds": [],
        "versions": [
            {
                "versionId": "48254f9a-80ab-4b09-b041-0671716d73d3",
                "fileReference": "5e1da94f1ab7e300017ab586",
                "fileSize": 159483693,
                "uploaded": "2020-01-14T11:53:47Z",
                "authorId": "5da480b75ed0570001d197e2",
                "authorName": "shankar.lakshman@solarenergy.com",
                "version": 1,
                "isArchived": false
            },
            {
                "versionId": "873b6fc9-6e62-4d8f-aac5-42c3aa8235a8",
                "fileReference": "5e1dad09b4ccd1000102e8cf",
                "fileSize": 159483693,
                "uploaded": "2020-01-14T12:04:22Z",
                "authorId": "5da480b75ed0570001d197e2",
                "authorName": "shankar.lakshman@solarenergy.com",
                "version": 2,
                "isArchived": false
            }
        ]        
    }
]
```