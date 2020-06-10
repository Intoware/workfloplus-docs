---
layout: page
title: Example Queries
permalink: /examples
nav_order: 99
---

# Example Queries
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

This page contains a number of example queries that you can use in the Query Designer. All of these queries can be copied directly into the Query Designer as-is to provide a starting block for your own queries.

## Get Latest Jobs

Gets the latest 20 jobs with some basic metadata.

*Note: The updated date is being renamed to `completed`*

```graphql
{
  jobs (limit: 20 order: "desc")
  {
    jobId               # ID of the job
    jobTitle            # Title of the job (possibly overriden by the user)
    workflowTitle       # Title of the workflow (if different from job title)
    created             # When the job was started
    completed: updated  # When the job was completed
    totalDuration       # Total Duration of the job in seconds
    userName            # Who completed the job
    geoLongAverage      # GPS Longitude of the job
    geoLatAverage       # GPS Latitude of the job
  }
}
```

## Get All Reports
{: .d-inline-block }

Coming Soon
{: .label .label-yellow }

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
## Get All Attachments (original file only)
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
## Get All Attachment Thumbnails

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
## Get Substep Tags

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
## Get Job Level Data

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

## Get All Users
{: .d-inline-block }
Coming Soon
{: .label .label-yellow }

Gets the list of all users and their groups

```graphql
{
  users {
    emailAddress
    name
    userGroups {
      name
    }
  }
}
```