---
layout: default
grand_parent: Sample API Parent
parent: Sample API Child
title: Sample API Granchild
nav_order: 1
nav_exclude: true
---

## HTTP Request

```
GET https://gateway.workfloplus.com/jobs/v1/{clientJobId}
```

## Path Parameters

| Columbo   | Type        |
| ----------- | ----------- |
| clientJobId | string      |
| clientJobId | string      |
| clientJobId | string      |

## Response Body
### JSON Representation
```
{
  "documentId": string,
  "replies": [
    {
      object (Response)
    }
  ],
  "writeControl": {
    object (WriteControl)
  }
}
```