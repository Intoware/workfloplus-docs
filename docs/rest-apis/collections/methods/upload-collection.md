---
layout: default
parent: Collections
title: Upload Collection
permalink: /collections/upload-collection
has_children: true
nav_order: 6
---


## Overview

The Collection Upload API provides a way to reliably upload files of upto 50mb by blocking them into a sequence of parts upto 100kb that can be uploaded individually.

By using this API the application uploads a file in part, allowing it to recover from a failed request more reliably. It means an application only needs to retry the upload of a single part instead of the entire file.

An additional benefit of blocked uploads is that parts can be uploaded in parallel, allowing for a potential performance improvement.

The process for uploading a collection file requires a couple of API calls to be made

1. [A Collection Upload Session is Created](./create-collection-upload-session.md): This session is used as a reference for the later calls and sets expectations for the block sizes and files sizes.

2. [File is Uploaded](./collection-upload-file.md): The file is uploaded as a series of blocks (N.B. if the file is small enough it can be uploaded as a single block).

## Notes
* Collection file size limit is 50 MB
* File block size limit is 100 KB
