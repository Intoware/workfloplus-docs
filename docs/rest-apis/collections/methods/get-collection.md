---
layout: default
parent: Collections
title: Get Collection
permalink: /collections/get-collection
nav_order: 1
---


## HTTP Request

```
GET https://accounts.workfloplus.com/collections/v1/collection/{collection_id}

```

## Authorization

*Bearer Token*

Policy
Any Valid Token


## Headers

| Key     | Value        |
| ----------- | ----------- |
| Authorization | Bearer {token}      |

## Path Parameters


| Parameter   | Type        |
| ----------- | ----------- |
| collection_id | string      |


## Response Body
### JSON Representation
```
{
  "collections":[
    {
      "collectionId":"5e8c434572v84700018ffb2c",
      "userId":"5d8cacd37811130001e71db0",
      "userName":"colin.pope@solarenergy.com",
      "created":"2020-04-07T09:09:25.082Z",
      "lastUpdated":"2020-04-07T09:09:25.082Z",
      "teamName":"collectionteam",
      "name":"Collection 1",
      "dataLastChanged":"2020-04-07T14:08:21.727Z",
      "headerNames":[
        "PenID",
        "AnimalID",
        "AnimalName",
        "InspectionTime"],
      "recordCount":0,
      "csvFileName":"5e8c895578c444000190048e",
      "csvFileSize":693,
      "csvFileNameHistory":{
        "5e8c434f78c84700018ffb30":"2020-04-07T09:09:35.563Z",
        "5e8c895578c847000190048e":"2020-04-07T14:08:21.727Z"
      },
      "csvDownloadUrl":"https://wfp27dev.blob.core.windows.net/collectionuploads/collectionteam/5e8c895578c444000190048e?sv=2019-02-02\u0026sr=b\u0026sig=RdqRRlqBxHzuTYBpYQhZyQ0wbBsPxGlWCa8PqnWH7EE%3D\u0026st=2021-09-14T05%3A41%3A53Z\u0026se=2021-09-14T06%3A46%3A53Z\u0026sp=r"
    }
  ]
}
```
