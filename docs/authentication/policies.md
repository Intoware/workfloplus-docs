---
layout: default
title: Policies
parent: Authentication
permalink: /authentication/policies

nav_order: 10
---

### Client_Admin


#### Scopes
* {{ site.policies_base_url }}/team.admin


#### Permissions
* OWNER



### Job_Modify


#### Scopes
* {{ site.policies_base_url }}/job.modify
* {{ site.policies_base_url }}/job.admin


#### Permissions
* OWNER



### Job_Read


#### Scopes
* {{ site.policies_base_url }}/job.read
* {{ site.policies_base_url }}/job.read_all
* {{ site.policies_base_url }}/job.admin


#### Permissions
* OWNER
* ADMIN



### Job_ReadAll


#### Scopes
* {{ site.policies_base_url }}/job.read_all
* {{ site.policies_base_url }}/job.modify
* {{ site.policies_base_url }}/job.admin


#### Permissions
* OWNER
* ADMIN



### Query_Admin


#### Scopes
* {{ site.policies_base_url }}/query.admin


#### Permissions
* OWNER
* ADMIN



### Query_Read


#### Scopes
* {{ site.policies_base_url }}/query.read
* {{ site.policies_base_url }}/query.admin


#### Permissions
* OWNER
* ADMIN



### Reports_Admin


#### Scopes
* {{ site.policies_base_url }}/reports.admin


#### Permissions
* OWNER
* ADMIN



### Reports_Create


#### Scopes
* {{ site.policies_base_url }}/reports.create
* {{ site.policies_base_url }}/reports.admin


#### Permissions
* OWNER
* ADMIN
* EDITOR



### Reports_Modify


#### Scopes
* {{ site.policies_base_url }}/reports.modify
* {{ site.policies_base_url }}/reports.admin


#### Permissions
* OWNER
* ADMIN



### Reports_Read


#### Scopes
* {{ site.policies_base_url }}/reports.read
* {{ site.policies_base_url }}/reports.create
* {{ site.policies_base_url }}/reports.admin


#### Permissions
* OWNER
* ADMIN
* EDITOR



### Schedule_Admin


#### Scopes
* {{ site.policies_base_url }}/schedule.admin


#### Permissions
* OWNER
* ADMIN



### Schedule_Read


#### Scopes
* {{ site.policies_base_url }}/schedule.read
* {{ site.policies_base_url }}/schedule.read_all
* {{ site.policies_base_url }}/schedule.admin


#### Permissions
* OWNER
* ADMIN



### Schedule_ReadAll


#### Scopes
* {{ site.policies_base_url }}/schedule.read_all
* {{ site.policies_base_url }}/schedule.admin


#### Permissions
* OWNER
* ADMIN



### Spoke_Client


#### Scopes
* {{ site.policies_base_url }}/spoke.client


#### Permissions
* SPOKE



### Team_Admin


#### Scopes
* {{ site.policies_base_url }}/team.admin


#### Permissions
* OWNER
* ADMIN



### TeamSettings_Admin


#### Scopes
* {{ site.policies_base_url }}/teamsettings.admin


#### Permissions
* OWNER
* ADMIN



### TeamSettings_Read


#### Scopes
* {{ site.policies_base_url }}/teamsettings.read
* {{ site.policies_base_url }}/teamsettings.admin


#### Permissions
* OWNER
* ADMIN
* EDITOR
* APPROVER



### Trigger_Admin


#### Scopes
* {{ site.policies_base_url }}/trigger.admin


#### Permissions
* OWNER
* ADMIN



### Trigger_Execute


#### Scopes
* {{ site.policies_base_url }}/workflow.execute
* {{ site.policies_base_url }}/workflow.admin


#### Permissions
* OWNER
* ADMIN



### Trigger_Read


#### Scopes
* {{ site.policies_base_url }}/trigger.read
* {{ site.policies_base_url }}/trigger.admin


#### Permissions
* OWNER
* ADMIN



### Workflow_Admin


#### Scopes
* {{ site.policies_base_url }}/workflow.admin


#### Permissions
* OWNER
* ADMIN



### Workflow_Approve


#### Scopes
* {{ site.policies_base_url }}/workflow.approve


#### Permissions
* APPROVER



### Workflow_Create


#### Scopes
* {{ site.policies_base_url }}/workflow.create
* {{ site.policies_base_url }}/workflow.admin


#### Permissions
* OWNER
* ADMIN
* EDITOR



### Workflow_Delete


#### Scopes
* {{ site.policies_base_url }}/workflow.delete
* {{ site.policies_base_url }}/workflow.admin


#### Permissions
* OWNER
* ADMIN
* EDITOR



### Workflow_Execute


#### Scopes
* {{ site.policies_base_url }}/workflow.execute


#### Permissions



### Workflow_Modify


#### Scopes
* {{ site.policies_base_url }}/workflow.modify
* {{ site.policies_base_url }}/workflow.admin


#### Permissions
* OWNER
* ADMIN
* EDITOR



### Workflow_Read


#### Scopes
* {{ site.policies_base_url }}/workflow.read
* {{ site.policies_base_url }}/workflow.execute
* {{ site.policies_base_url }}/workflow.admin
* {{ site.policies_base_url }}/spoke.client


#### Permissions
* OWNER
* ADMIN
* EDITOR
* APPROVER
* SPOKE

