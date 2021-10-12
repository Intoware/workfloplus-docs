---
layout: default
parent: Report Templates
title: Get Report Template
permalink: /reporttemplates/get-report-template
nav_order: 2
---

## HTTP Request
```
GET {{ site.main_api_base_url }}/reporttemplates/v1/content/{reportTemplate_id}
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


## Response Body
### JSON Representation
```
{
  "reportTemplateId":"615fff0b1b4ee200018fe357",
  "name":"Report Template Example 1",
  "description":null,
  "headerContent":"<header>\n</header>",
  "bodyContent":"<!doctype html>\n<html lang=\"en\">\n  <head>\n<meta charset=\"utf-8\">\n
                 <style type=\"text/css\"></style>\n  </head>\n  <body>
                 <h1> Api Testing Report Template </h1></body>\n</html>",
  "lastUpdated":"2021-10-08T13:19:14Z",
  "userId":"5d8cac54860b8100016b1987",
  "options":{
    "isLandscape":false,
    "title":"Report Template Example 1",
    "headerHeight":48,
    "hideFooter":false},
  "isDefault":false,
  "isArchived":false,
  "metadata":{}
}
```

