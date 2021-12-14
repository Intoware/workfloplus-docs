---
layout: default
parent: Reports
title: Get PDF by Client Job Id
permalink: /reports/get-pdf-by-clientJobId
nav_order: 1
---

## HTTP Request
```
GET {{ site.main_api_base_url }}/reports/v1/generate/{clientJobId}
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
| getUrlOnly | boolean      |

## Path Parameters

| Parameter   | Type        |
| ----------- | ----------- |
| clientJobId        | string      |

## Response Body
### JSON Representation
```
https://wfp27dev.blob.core.windows.net/reportpdfs/testteam/615af46c3e96ba0001c4067
_5eb113b42faf0f254b092de7?sv=2019-02-02&sr=b&sig=%2FYxBFVIs62iHEv73Aw9kzLZ9pJmirUP
WHlSngQQc7Po%3D&st=2021-12-10T12%3Aw8%3A23Z&se=2021-12-10T13%3A13%3A23Z&sp=r

```
