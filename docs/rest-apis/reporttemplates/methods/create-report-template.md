---
layout: default
parent: Report Templates
title: Create Report Template
permalink: /reporttemplates/create-report-template
nav_order: 8
---

## HTTP Request
```
POST {{ site.main_api_base_url }}/reporttemplates/v1/content
```
## Authorization

*Bearer Token*

Policy
[Reports_Create]({{site.url}}{{site.baseurl}}/authentication/policies#reports_create)

## Headers

| Key     | Value        |
| ----------- | ----------- |
| Authorization | Bearer {token}      |

## Request Body
### JSON Representation
```
{
  "name":"APi Template Example 1",
 "headerContent":"<header>\n</header>",
 "bodyContent":"<!doctype html>\n<html lang=\"en\">\n\n  <head>\n <meta charset=\"utf-8\">\n  
                <style type=\"text/css\">\n </style>\n  </head>\n\n <body>\n\n  </body>\n\n</html>",
 "options":{"headerHeight":48,"title":"APi Template Example 1"}
}
```

## Response Body
### JSON Representation
```
{
  "reportTemplateId":"61652831013a4200010e5405",
  "name":"APi Template Example 1",
  "description":null,
  "headerContent":"<header>\n</header>",
  "bodyContent":"<!doctype html>\n<html lang=\"en\">\n\n  <head>\n <meta charset=\"utf-8\">\n 
                 <style type=\"text/css\">\n </style>\n  </head>\n\n <body>\n\n  </body>\n\n</html>",
  "lastUpdated":"0001-01-01T00:00:00",
  "userId":null,
  "options":{
    "isLandscape":false,
    "title":"APi Template Example 1",
    "headerHeight":48,
    "hideFooter":false
  },
  "isDefault":false,
  "isArchived":false,
  "metadata":{
  }
}
```

