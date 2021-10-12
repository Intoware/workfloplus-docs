---
layout: default
parent: Report Templates
title: Get All Report Templates
permalink: /reporttemplates/get-all-report-templates
nav_order: 1
---

## HTTP Request
```
GET {{ site.main_api_base_url }}/reporttemplates/v1
```
## Authorization

*Bearer Token*

Policy
[Reports_Create]({{site.url}}{{site.baseurl}}/authentication/policies#reports_create)

## Headers

| Key     | Value        |
| ----------- | ----------- |
| Authorization | Bearer {token}      |

## Response Body
### JSON Representation
```
[
  {
    "reportTemplateId":"5ec4f0fde9efaa03011a07bc",
    "name":"Example Report 1",
    "description":"To demo report templates apis",
    "template":{
      "templateId":"601291dd90a363400112c636",
      "templateBodyFile":{
        "name":"Body template",
        "uri":"1e74cc05-3304-497b-9690-35481cd61149",
        "contentType":"text/html",
        "downloadUrl":"https://wfp27dev.blob.core.windows.net/reporttemplates/testteam/1e74cc05-4304-497b-9690-35481cd61349?sv=2019-02-02&sr=b&sig=AKhrBbbunmVDpI%2BEtUlITA39HZ5G5j0ycMP3%2FGaHfek%3D&st=2021-10-08T07%3A10%3A11Z&se=2021-10-08T08%3A15%3A11Z&sp=r"},
      "templateHeaderFile":{
        "name":"Header template",
        "uri":"f42d00af-b807-4d57-8aba-124e2fad80cf",
        "contentType":"text/html",
        "downloadUrl":"https://wfp27dev.blob.core.windows.net/reporttemplates/testteam/f42e40af-b217-4d57-8aba-124e2fad80cf?sv=2019-02-02&sr=b&sig=Z7%2B3hKXQFIUioVZKN4Gz5bQa5ZfVsJlKbEdxT4t7VzI%3D&st=2021-10-08T07%3A10%3A11Z&se=2021-10-08T08%3A15%3A11Z&sp=r"},
      "uploadedDate":"2021-01-28T10:28:45Z",
      "userId":"5d8cacd378411f0321e71db0"},
    "lastUpdated":"2021-01-28T10:28:45Z",
    "options":{
      "isLandscape":false,
      "title":"Example Report 1",
      "headerHeight":48,
      "hideFooter":false},
    "isDefault":false,
    "isArchived":false,
    "metadata":{}
  },
  {
    "reportTemplateId":"5f036028e031440091c9a073",
    "name":"Example Report 2",
    "description":null,
    "template":{
      "templateId":"5f0432c4e031440001c9c8e6",
      "templateBodyFile":{
        "name":"Body template",
        "uri":"1c0d47f0-1e6f-41f4-893d-0233df06a332",
        "contentType":"text/html",
        "downloadUrl":"https://wfp27dev.blob.core.windows.net/reporttemplates/testteam/1c0d47f0-1e6f-41f4-893d-0233df06a332?sv=2019-02-02&sr=b&sig=S%2FbmcGnJm9gUJ7%2F4ZzlX1J7sCwzh4ca%2BxhmN5EEaV5c%3D&st=2021-10-08T07%3A10%3A11Z&se=2021-10-08T08%3A15%3A11Z&sp=r"},
      "templateHeaderFile":{
        "name":"Header template",
        "uri":"46e29592-66f1-468b-9cad-cac35be1a0e0",
        "contentType":"text/html",
        "downloadUrl":"https://wfp27dev.blob.core.windows.net/reporttemplates/testteam/46e22592-66f1-468b-9cad-cace5be1a0e0?sv=2019-02-02&sr=b&sig=RhrtxbjJzi8klOHjkyTLB7ug%2BQnfz%2BsD28l3p%2FzFhpY%3D&st=2021-10-08T07%3A10%3A11Z&se=2021-10-08T08%3A15%3A11Z&sp=r"},
      "uploadedDate":"2020-07-07T08:31:00Z",
      "userId":"5e21df72e7fb2433011f12fd"},
    "lastUpdated":"2020-07-14T07:27:24Z",
    "options":{
      "isLandscape":false,
      "title":"Example Report 2",
      "headerHeight":48,
      "hideFooter":false},
    "isDefault":false,
    "isArchived":false,
    "metadata":{
      "jobId":"5f0d5ac0bafw9b00013c2495",
      "workflowId":"a1d4234f-f67d-49f6-92e5-2fc0c4d08643"}
  }
]
```

