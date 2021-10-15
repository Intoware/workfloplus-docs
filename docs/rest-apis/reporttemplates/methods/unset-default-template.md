---
layout: default
parent: Report Templates
title: Unset Default Report Template
permalink: /reporttemplates/unset-default-template
nav_order: 7
---

## HTTP Request
```
PUT {{ site.main_api_base_url }}/reporttemplates/v1/default/unset
```
## Authorization

*Bearer Token*

Policy
[Reports_Create]({{site.url}}{{site.baseurl}}/authentication/policies#reports_create)

## Headers

| Key     | Value        |
| ----------- | ----------- |
| Authorization | Bearer {token}      |
