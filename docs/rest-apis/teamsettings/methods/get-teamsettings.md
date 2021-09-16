---
layout: default
parent: TeamSettings
title: Get TeamSettings
permalink: /teamsettings/get-teamsettings
nav_order: 3
---


## HTTP Request

```
GET {{ site.main_api_base_url }}/teamsettings/v1/
```


## Authorization

*Bearer Token*

Policy
[TeamSettings_Read]({{site.url}}{{site.baseurl}}/authentication/policies#teamsettings_read)


## Headers

| Key     | Value        |
| ----------- | ----------- |
| Authorization | Bearer {token}      |

## Response Body
### JSON Representation
```
{
  "AutoDeviceSignOut":null,
  "AutoDownload":{
    "WorkflowUpdateMode":"Optional",
    "WorkflowUpdateLapsedTime":0
  },
  "CheckDeviceTime":false,
  "DefaultTimezone":"Etc/UTC",
  "DisableJobRestart":true,
  "DisableOldTemplates":false,
  "EnableJobNaming":false,
  "GoBackReason":"Optional",
  "PermanentDataEdit":false,
  "RemoteExpertSolution":null,
  "Reports":{
    "DefaultReport":null
  },
  "RequiresAbandonReason":false,
  "StoreDBOnExternalStorage":false,
  "SupportsOnsight":false,
  "WorkflowApproverMode":0
}
```
