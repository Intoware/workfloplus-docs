---
layout: default
parent: Report Templates
title: Get Default Template
permalink: /reporttemplates/get-default-template
nav_order: 4
---

## HTTP Request
```
GET {{ site.main_api_base_url }}/reporttemplates/v1/default
```
## Authorization

*Bearer Token*

Policy
[Reports_Create]({{site.url}}{{site.baseurl}}/authentication/policies#reports_create)

## Headers

| Key     | Value        |
| ----------- | ----------- |
| Authorization | Bearer {token}      |