---
layout: default
title: Upload a Workflow
parent: Workflows
permalink: /workflows/upload
has_children: true
nav_order: 4
---

## Overview

As Workflow files have the potential to be quite large; primarily when they include large assets such as videos, images and files,
The Workflow Upload API provides a way to reliably upload those files by blocking them into a sequence of parts that can be uploaded individually.


By using this API the application uploads a file in part, allowing it to recover from a failed request more reliably. It means an application only needs to retry the upload of a single part instead of the entire file.


An additional benefit of blocked uploads is that parts can be uploaded in parallel, allowing for a potential performance improvement.


The process for uploading a Workflow requires a sequence of API calls to be made

1. [A Workflow Upload Session is Created](./create-workflow-upload-session.md): This session is used as a reference for the later calls and sets expectations for the block sizes and files sizes.

2. [File blocks are Uploaded](./workflow-upload-block.md): The file is uploaded as a series of blocks (N.B. if the file is small enough it can be uploaded as a single block).

3. [The Workflow Upload Session is Completed](./finalise-workflow-upload.md): This call is made once all blocks have successfully been uploaded, it closes the session and defines metadata on the Workflow.



## Example

I have a file of size 150 KB which I will uploaded in blocks of 100 KB, I multiply both of these by 1024 to calculate the file size and block size

```
BLOCKSIZE = 102400
FILESIZE = 153600
```


I make an initial call to create the workflow upload session
```curl
curl -XPOST
-H 'Authorization: Bearer eyJhbGciOiJSUzI1NiIsImtpZCI6...'
-H "Content-type: application/json"
-d '{"blockSize": 102400, "fileSize": 153600, "friendlyFileName": "Workflow1.zip"}'
'{{ site.main_api_base_url }}/workflows/v2/upload'
```


As a response I receive an Id for the upload session
```
{
    "id": "60578b426a9eb4000114ec13"
}
```


I then make two seperate calls for each block, each referencing the upload session Id in the Url.
The first uploads the first 100 KB and the second the remaining 50 KB (N.B. the order of upload is not important)
#### Block 1 
```curl
curl -XPOST
-H 'Authorization: Bearer eyJhbGciOiJSUzI1NiIsImtpZCI6...'
-H 'Content-Length: 102400'
-H 'Content-Range: bytes 0-102399/153600'
-d 'PK\x03\x04\x14\x00\x00\x00\x08\x00...'
'{{ site.main_api_base_url }}/workflows/v2/upload/60578b426a9eb4000114ec13'
```
#### Block 2 
```curl
curl -XPOST
-H 'Authorization: Bearer eyJhbGciOiJSUzI1NiIsImtpZCI6...'
-H 'Content-Length: 102400'
-H 'Content-Range: bytes 102400-153599/153600'
-d '\xf7\xfb\xb7\x05x\xea~\x01\xdf\...'
'{{ site.main_api_base_url }}/workflows/v2/upload/60578b426a9eb4000114ec13'
```


Once those are both completed I then complete the upload session by defining the metadata for the workflow
```curl
curl -XPOST
-H 'Authorization: Bearer eyJhbGciOiJSUzI1NiIsImtpZCI6...'
-H "Content-type: application/json"
-d '{ "uploadId": "60578b426a9eb4000114ec13", "name": "My First Workflow" }'
'{{ site.main_api_base_url }}/workflows/v2'
```