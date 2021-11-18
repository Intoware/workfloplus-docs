---
layout: default
title: Permissions, Scopes & Policies
parent: Authentication
permalink: /authentication/permissions

nav_order: 20
---

## Permissions, Scopes & Policies

Three concepts need to be outlined in order to understand whether a request will be authorized.

### Policies

Each API will have a Policy defined against it, in order to be authorized a request will have to meet the requirements of that Policy; a Policy includes a list of Scopes and Permissions, in order to meet the requirements of that Policy the request will need to include a match to at least one of the Scopes and one of the Permissions.

### Permissions

Permissions reside with the user or client, they define the level of and types of action that the user/client can take along with the data that they can access

### Scopes

Scopes reside with the token, they define the level of and types of action that the user/client can take along with the data that they can access

### Example

Consider an application that primarily reads and reports data for a given service but occasionally is required to modify data on that service; in order to perform the full range of actions the client created for this application would probably need a high level Permission such as ADMIN, however the developer of the integration may decide to request and cache a token that includes only the {{ site.policies_base_url }}/xxx.read Scope in order to read the data whenever required and then on the occasions where data modification is required a one-off token could be generated that includes the {{ site.policies_base_url }}/xxx.modify Scope. This follows the principle of least privilege, a key principle for secure systems.