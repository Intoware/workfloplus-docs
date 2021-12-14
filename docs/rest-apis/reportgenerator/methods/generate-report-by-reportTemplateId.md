---
layout: default
parent: Report Generator
title: Generate Report by Report Template Id
permalink: /reportgenerator/generate-report-by-reportTemplateId
nav_order: 2
---

## HTTP Request
```
POST {{ site.main_api_base_url }}/reportgenerator/v1/generate/{reportTemplateId}?{jobId}
```
## Authorization

*Bearer Token*

Policy
[Reports_Read]({{site.url}}{{site.baseurl}}/authentication/policies#reports_read)

## Headers

| Key     | Value        |
| ----------- | ----------- |
| Authorization | Bearer {token}      |

## Query Parameters

| Parameter   | Type        |
| ----------- | ----------- |
| jobId | string      |

## Path Parameters

| Parameter   | Type        |
| ----------- | ----------- |
| reportTemplateId        | string      |

## Response Body
### JSON Representation
```
{
  "jobId":"615af46c3396ba2001e40675",
  "status":"Completed",
  "reportUrl":"https://wfp27dev.blob.core.windows.net/reportpdfs/apiteam/615af46c3396ba0301c40675_5eb113b42faf0f254b192de7?sv=2019-02-02&sr=b&sig=y068gzJ0upmCwSwwXD7EMh0Qggz9IRpjTTCsSOtq5nE%3D&st=2021-12-09T13%3A41%3A42Z&se=2021-12-09T14%3A46%3A42Z&sp=r"
}

```
