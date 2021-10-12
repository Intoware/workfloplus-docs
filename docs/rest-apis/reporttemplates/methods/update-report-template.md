---
layout: default
parent: Report Templates
title: Update Report Template
permalink: /reporttemplates/update-report-template
nav_order: 9
---

## HTTP Request
```
PUT {{ site.main_api_base_url }}/reporttemplates/v1/content/{reportTemplate_id}
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
  "reportTemplateId":"61652831017a4200010e5405",
  "name":"APi Template Example 1",
  "description":null,
  "headerContent":"<header>\n</header>",
  "bodyContent":"<!doctype html>\n<html lang=\"en\">\n  <head>\n    <meta charset=\"utf-8\">\n    
                 <style type=\"text/css\"></style>\n  </head>\n  <body> 
                 <h1> Updated Via Api Call </h1>  </body>\n</html>",
  "lastUpdated":"2021-10-12T06:29:23Z",
  "userId":"5d8cac54860b8100016b1987",
  "options":{"isLandscape":false,
             "title":"APi Template Example 1",
             "headerHeight":48,
             "hideFooter":false},
  "isDefault":false,
  "isArchived":false,
  "metadata":{}
}
```

