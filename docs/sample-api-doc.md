---
layout: default
parent: Sample API Parent
title: Sample API Child
has_children: true
nav_order: 1
nav_exclude: true
---

## HTTP Request

```
GET https://gateway.workfloplus.com/jobs/v1/{clientJobId}
```

## Path Parameters
| Parameter   | Type        |
| ----------- | ----------- |
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