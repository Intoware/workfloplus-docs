---
layout: page
title: Querying Jobs
permalink: /jobquery
nav_order: 11
---

# Querying Jobs
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---


# Introduction
Querying for Jobs is the most common application of the WorkfloPlus Query API

## Starting a Query
The base query structure for a job query is as follows (N.B. this query alone will not work as at least one field must be specified)
```graphql
{
    jobs
    {
        
    }
}
```

# Filtering on specific Jobs
By default the query will return the first 100 completed jobs for your team; however there are several query parameters that can be used to filter the query to return only the required jobs

## Filtering on Workflow(s)
There are several options for filtering on workflows but you can only apply one of them

**Filtering on WorkflowId(s)**
If you wish to match on one or more workflow Ids you can add this as part of the query
```graphql
{
    jobs(workflowId: "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")
    {
        
    }
}
```
```graphql
{
    jobs(workflowId: ["xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy"])
    {
        
    }
}
```

**Filtering on Workflow Title(s)**
If you wish to match on one or more workflow titles you can add this as part of the query
```graphql
{
    jobs(workflowTitle: "Inspection A")
    {
        
    }
}
```
```graphql
{
    jobs(workflowTitle: ["Inspection A", "Inspection B"])
    {
        
    }
}
```

**Filtering on Workflow Tag(s)**
If you wish to match on one or more workflow tags you can add this as part of the query; when matching on multiple workflows you can either match workflows that have at least one of the tags listed (workflowTagsOr) or alternatively only on workflows that have all of the tags listed (workflowTagsAnd)
```graphql
{
    jobs(workflowTag: "Inspection")
    {
        
    }
}
```
```graphql
{
    jobs(workflowTagsOr: ["Inspection", "Repair"])
    {
        
    }
}
```
```graphql
{
    jobs(workflowTagsAnd: ["Inspection", "Site A", "Mechanical"])
    {
        
    }
}
```


## Filtering on User(s)
There are two options for filtering on the user that completed a job but you can only apply one of them

**Filtering on Username(s)**
If you wish to match on one or more usernames you can add this as part of the query
```graphql
{
    jobs(userName: "anne.worker@repairs.com")
    {
        
    }
}
```
```graphql
{
    jobs(userName: ["inspector1@repairs.com", "inspector2@repairs.com"]
    {
        
    }
}
```

**Filtering on UserId(s)**
If you wish to match on one or more user Ids you can add this as part of the query
```graphql
{
    jobs(userId: "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")
    {
        
    }
}
```
```graphql
{
    jobs(userId: ["xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy"])
    {
        
    }
}
```

## Filtering on Job Identifier(s)
There are two options for filtering on specific job identifiers but you can only apply one of them

**Filtering on Job Titles(s)**
If you wish to match on one or more job titles you can add this as part of the query
```graphql
{
    jobs(jobTitle: "Inspection 3A/5F")
    {
        
    }
}
```
```graphql
{
    jobs(jobTitle: ["Inspection 3A/5F", "Inspection 3A/5G"])
    {
        
    }
}
```

**Filtering on JobId(s)**
If you wish to match on one or more job Ids you can add this as part of the query
```graphql
{
    jobs(jobId: "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")
    {
        
    }
}
```
```graphql
{
    jobs(jobId: ["xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy"])
    {
        
    }
}
```

## Filtering on Date and Time
There are options for filtering on the date and time that a job was both created and updated and also on, any combination of the following can be applied together

**Filtering on jobs created since a given date and time**
If you wish to filter on jobs created since a given date and time you can specifiy that as an ISO format datetime 
```graphql
{
    jobs(createdSince: "2019/06/01T08:00:00.000Z")
    {
        
    }
}
```

**Filtering on jobs created before a given date and time**
If you wish to filter on jobs created before a given date and time you can specifiy that as an ISO format datetime 
```graphql
{
    jobs(createdBefore: "2019/06/01T08:00:00.000Z")
    {
        
    }
}
```

**Filtering on jobs updated since a given date and time**
If you wish to filter on jobs updated since a given date and time you can specifiy that as an ISO format datetime 
```graphql
{
    jobs(updatedSince: "2019/06/01T08:00:00.000Z")
    {
        
    }
}
```

**Filtering on jobs updated before a given date and time**
If you wish to filter on jobs updated before a given date and time you can specifiy that as an ISO format datetime 
```graphql
{
    jobs(updatedBefore: "2019/06/01T08:00:00.000Z")
    {
        
    }
}
```

## Limit, Order & Pagination

By default a query on the Jobs model will return data for up to the first 100 jobs that meet the criteria of the filter, however this number can be specified using the limit parameter, any value between 1 and 1000 is allowed.

By default a query on the Jobs model will return data for the first n jobs however the order of the data can be controlled using the order parameter; this is equivalent to setting order = "asc", setting the order = "desc" will return the last n jobs.

As the number of jobs increases it becomes inefficient to pull down the entire data set everytime a data update is required, instead it is recommended to build your own store of the data. Pagination is the process of taking the data piece by piece to build up a full data set. We support a cursor based pagination solution, whereby everytime you query the data you can get the completedJobCursor for each job, cache the cursor for the last job in the list and then pass that back as a parameter next time you run the query to get the next n jobs.

```graphql
{
    jobs(limit: 1000 order: "desc" cursor: "5e3036f5e456fc00012e2b89")
    {
        
    }
}
```

# Selecting Job Fields

## Selecting Fields on the Job Level
There are a range of fields on the job level that can be included in the query and returned
```graphql
{
    jobs
    {
        jobId
        completedJobCursor    # Cursor to be used for data pagination, relates to the timestamp at which the job was uploaded
        teamName
        workflowId
        workflowVersionId
        workflowTitle
        workflowTags
        jobTitle
        created
        updated
        totalDuration         # Total Duration given in Seconds
        activeDuration        # Active Duration given in Seconds (equivalent to the Total Duration minus any period where the Job was paused)
        status
        userId
        userName
        geoLongAverage        # Median average longitude across all completed steps
        geoLatAverage         # Median average latitude across all completed steps
        metadata              # Any metadata attached to the job displayed as an array of name value pairs
        {
            name
            value
        }
    }
}
```

## Selecting Fields on the Steps Level
Additionally the Steps field can be included on the Job level, this then returns an array of information for each step
```graphql
{
    jobs
    {
        jobId
        steps
        {
            stepId
            uniqueStepId
            stepTitle
            stepDescription
            stepType
            started
            completed
            cancelled
            isCancelled
            isFormStep
            totalDuration
            activeDuration
            userId
            userName
            geoLat
            geoLong
            formLoopIteration
            note
            values
            value
        }
    }
}
```

## Selecting Fields on the Substeps Level
Many users will not need to consider to substeps level and will be able to build all queries at the steps level. Substeps apply where Form Steps are used, here we have the concept of steps within steps and the substeps level allows you to break out the detail at each substep within a form.
```graphql
{
    jobs
    {
        steps
        {
            substeps
            {
                stepId
                uniqueStepId
                stepTitle
                stepDescription
                stepType
                stepTag
                values
                value
            }
        }
    }
}
```

## Selecting Specific Steps
Specific steps can be selected to be returned in the query and named at the same time

**Step Search**
A search term can be applied to the steps array, this will look for an exact match against each stepId, stepTag and then stepTitle. If none are found it will return null, if one or more matches are found it will return the first match that it finds.

The following query will return the jobId for each job, then the specified information for the first step that it finds that has a tag or title that matches "Instruction", then the specified information for the first step that it finds that has one of the stepIds in the list shown

```graphql
{
  jobs
  {
    jobId
    InstructionStep:step(search: "Instruction")
    {
      stepId
      stepTitle
      totalDuration
    }
    RepairDetailsStep:step(search: ["a1cee52e-e950-4894-9f49-9e95862bb9a9", "a1cee52e-e950-4894-9f49-9e95862bb9a1"])
    {
      stepId
      stepTitle
      totalDuration
    }
  }
}
```

**Step Regex Search**

Regex search works much like search except it can only match against a single term, however it can apply regex patterns for matching making it more powerful.

The following query will return the jobId for each job, then the specified information for the first step that it finds that includes the word "HSSE" anywhere in the step tag or title

Documentation on [regex patterns can be found here](https://docs.microsoft.com/en-us/dotnet/standard/base-types/regular-expression-language-quick-reference).

```graphql
{
  jobs
  {
    jobId
    HsseStep:step(regexSearch: "HSSE")
    {
      stepId
      stepTitle
      totalDuration
    }
  }
}
```

# Select Job Attachments

The attachments comprise all of the photos, images, videos, files etc that have been captured for a given job, there are differetne approaches available for constructing a query to extract your attachments

## Get All Attachments on a Job

The most convinient way to simply extract details of all of the attachments on a job is to use the attachments field on the job
```graphql
{
  jobs
  {
    jobId
    attachments
    {
      attachmentId
      # ...otherfields...
    }
  }
}
```

## Get Attachments on a Step or Substep

Alternatively attachment details can be returned on the step or substep on which they were captured
```graphql
{
    jobs
    {
        jobId
        steps
        {
            attachments
            {
                attachmentId
                # ...otherfields...
            }
        }
    }
}
```
```graphql
{
    jobs
    {
        jobId
        steps
        {
            substeps
            {
                attachments
                {
                    attachmentId
                    # ...otherfields...
                }
            }
        
    }
}
```

## Attachment Model
The attachment model provides details of both the original attachment and additionally any thumbnails that WorkfloPlus has generated; if you query a job shortly after it has been completed you may find that all attachments and thumbnails are not present in the result as they are still syncing or being generated
```graphql
{
  jobs
  {
    jobId
    attachments
    {
      attachmentId
      stepId
      uniqueStepId
      stepTitle
      mimeType
      fileSize
      downloadUrl
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
The downloadUrl for each attachment and each thumbnail is a temporary URL that can be used to download the file itself, for example if the response contains a downloadUrl
```
...
"fileSize": 14204,
"downloadUrl": "https://wfp.blob.core.windows.net/stepresources/myteam/63e39d97-d6cb-433b-b69c-2e2ed6c76f37?sv=2019-02-02&sr=b&sig=HgS7dodYUEinIr3dXE%2BSH5isA3BBe8bZREg2I6m%2FvCo%3D&st=2020-06-17T14%3A55%3A56Z&se=2020-06-17T16%3A00%3A56Z&sp=r",
...
```
That downloadUrl can be used in a Http request; the snippet below uses a downloadUrl returned by a query to save an attachment to a file called "myattachmentfile"
```
curl "https://wfp.blob.core.windows.net/stepresources/myteam/63e39d97-d6cb-433b-b69c-2e2ed6c76f37?sv=2019-02-02&sr=b&sig=HgS7dodYUEinIr3dXE%2BSH5isA3BBe8bZREg2I6m%2FvCo%3D&st=2020-06-17T14%3A55%3A56Z&se=2020-06-17T16%3A00%3A56Z&sp=r" --output myattachmentfile
```
If the downloadUrl expires a new one can be generated by re-querying the data