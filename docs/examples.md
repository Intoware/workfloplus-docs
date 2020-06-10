---
layout: page
title: Example Queries
permalink: /docs/examples
nav_order: 99
has_toc: true
---

# Example Queries
This page contains a number of example queries that you can use in the Query Designer. All of these queries can be copied directly into the Query Designer as-is to provide a starting block for your own queries.

### Get All Reports
Gets the latest 5 jobs containing with a list of generated PDF reports and their download link.

```graphql
{
  jobs (limit: 5 order: "desc")
  {
    jobId
    jobTitle
    reports
    {
      generatedReportId
      generated
      templateName
      mimeType
      downloadUrl
    }
  }
}
```
​
### Get All Attachments (original file only)
Gets the latest 5 jobs containing a list of all received attachments along with download links and metadata.

*Note: See below for an example on Thumbnails*

```graphql
{
  jobs (limit: 5 order: "desc")
  {
    jobId
    jobTitle
    attachments
    {
      attachmentId
      stepId
      uniqueStepId
      stepTitle
      mimeType
      fileSize
      downloadUrl
    }
  }
}
```
​
### Get All Attachment Thumbnails

For the latest 5 jobs, gets their attachments and any thumbnails generated. Usually there are 3 JPEG thumbnails (small, medium and large) generated for each image and video.

```graphql
{
  jobs (limit: 5 order: "desc")
  {
    jobId
    jobTitle
    attachments
    {
      attachmentId
      thumbnails
      {
        name
        created
        mimeType
        fileSize
        width
        height
        downloadUrl
      }
    }
  }
}
```
​
### Get Substep Tags

For the latest 5 jobs, get a list of all step tags captured during execution.

```graphql
{
  jobs (limit: 5 order: "desc")
  {
    jobId
    jobTitle
    steps
    {
      substeps
      {
        stepTag
      }
    }
  }
}
```
​
​
### Get Job Level Data

For the latest 5 jobs, gather more detailed metadata on the job.

```graphql
{
  jobs (limit: 5 order: "desc")
  {
    jobId
    completedJobCursor
    teamName
    workflowId
    workflowVersionId
    workflowTitle
    workflowTags
    jobTitle
    created
    updated
    totalDuration
    activeDuration
    status
    userId
    userName
    geoLongAverage
    geoLatAverage
    metadata
    {
      name
      value
    }
  }
}
```