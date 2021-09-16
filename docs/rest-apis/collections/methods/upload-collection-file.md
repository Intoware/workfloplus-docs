---
layout: default
grand_parent: Collections
parent: Upload Collection
title: Upload Collection File
permalink: /collections/upload-collection/upload-collection-file
nav_order: 2
---


## HTTP Request

```
POST {{ site.main_api_base_url }}/collections/v1/upload/{upload_id}
```

## Authorization

*Bearer Token*

Policy
[Workflow_Create]({{site.url}}{{site.baseurl}}/authentication/policies#workflow_create)

## Headers

| Key     | Value        |
| ----------- | ----------- |
| Authorization | Bearer {token}      |
| Content-Type | text/csv      |
| Content-Length | {blockSize}      |
| Content-Range | bytes {i x blockSize}-{(i+1) x blockSize}-1/{fileSize} |

## Path Parameters


| Parameter   | Type        |
| ----------- | ----------- |
| upload_id | string      |



## Request Body
```
{block_bytes}
```


## Response Body
### If the block was the final block and all blocks been uploaded a 204 is returned
### If the block was not the final block but has been uploaded a 202 is returned


## Notes
I have a file of size 150 KB which I will uploaded in blocks of 100 KB, I multiply both of these by 1024 to calculate the file size and block size 

```
BLOCKSIZE = 102400
FILESIZE = 153600
```

