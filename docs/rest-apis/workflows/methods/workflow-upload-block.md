---
layout: default
grand_parent: Workflows
parent: Upload a Workflow
title: Upload Workflow Block
permalink: /workflows/upload/workflow-upload-block
nav_order: 2
---


## HTTP Request

```
POST https://gateway.workfloplus.com/workflows/v2/upload/{uploadId}
```

## Authorization

*Bearer Token*

Policy
[Workflow_Create]({{site.url}}{{site.baseurl}}/authentication/policies#workflow_create)

## Headers

| Key     | Value        |
| ----------- | ----------- |
| Authorization | Bearer {token}      |
| Content-Length | {BLOCKSIZE}      |
| Content-Range | bytes {i x BLOCKSIZE}-{(i+1) x BLOCKSIZE}/{FILESIZE}     |


## Request Body
```
{block_bytes}
```


## Response Body
### If the block was the final block and all blocks been uploaded a 204 is returned
### If the block was not the final block but has been uploaded a 202 is returned


## Notes
* Workflow file size limit is 200 MB
* File chunk size limit is 100 KB