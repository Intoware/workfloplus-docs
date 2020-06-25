---
layout: page
title: Ingest Data to Excel
permalink: /excelexample
nav_order: 12
---

## Ingest WorkfloPlus Data to Excel    
![WorkfloPlus Excel](assets/workfloplus-excel.png)
The WorkfloPlus GraphQL Query API supports integration with many tools; one of the more common requests is for users to extract their data from WorkfloPlus into Excel.
This example outlines an approach for not only ingesting data into Excel but moreover for creating a live link between Excel and WorkfloPlus so that the data set can be refreshed on demand from within Excel.

### 1. Create the Query
In the following example selected data is extracted for each Inspection & Maintenance activity that is carried out.
The query includes only jobs that are completed on the "Component Inspection & Maintenance" workflow.
For each job the query extracts selected information from the job and in addition it extracts defined fields on specified steps; for example on the _componentCodeStep_ the value that is input is extracted as this is of interest, whereas on the _maintenanceStep_ it is the step duration that is of interest and so this is specified in the query.
```graphql
{
    jobs(workflowTitle: "Component Inspection & Maintenance" limit: 50 order: "desc")
    {
        jobId
        jobTitle
        workflowId
        workflowTitle
        userName
        created
        updated
        totalDuration
        activeDuration
        geoLongAverage
        geoLatAverage
        componentCodeStep: step(search: "componentcode")
        {
            value
        }
        conditionBeforeStep: step(search: "bd9a9c4a-0784-4f7c-9ccb-7c1f8739a3d9")
        {
            substeps
            {
                stepTitle
                value
            }
        }
        runningTemperatureBeforeStep: step(search: "beforemaintenancerunningtemperature")
        {
            value
        }
        maintenanceStep: step(search: "ComponentMaintenance")
        {
            activeDuration
        }
        conditionAfterStep: step(search: "300d2f14-6a56-4ae4-a754-d017d8369376")
        {
            substeps
            {
                stepTitle
                value
            }
        }
        runUpStep:step(search: "Runup")
        {
            totalDuration
        }
        runningTemperatureAfterStep: step(search: "aftermaintenancerunningtemperature")
        {
            value
        }
    }
}
```

![WorkfloPlus Query Designer - Excel Example Query](assets/excel-example-query.png)
*Create the Query in the Query Designer*


### 2. Select the Output Format
The defacto output format for a GraphQL query and for any HTTP request is JSON; Excel does support the conversion of JSON into tabular data however to make the process more convenient WorkfloPlus also allows the user to extract the data in a flat format CSV, more information on setting the output format can be found [here.](https://intoware.github.io/workfloplus-docs/query-designer#csv-queries)

### 3. Execute Query from Excel
Microsoft's documentation on querying data from a web source can be found [here](https://support.office.com/article/import-data-from-external-data-sources-power-query-be4330b3-5356-486c-a168-b68e9e616f5a), the approach varies depending on the version of Excel. The example here uses version 16 of Excel.
Start a blank workbook, select the _Data_ ribbon and then from within the Data ribbon select _From Web_. From the Query Designer [copy the url for your query](https://intoware.github.io/workfloplus-docs/query-designer#exporting-queries), ensuring you use the GET request method along with the CSV format option and then paste the url into the dialog box that has opened in Excel.
![Excel - Excel Enter Data Source](assets/excel-enter-data-url.png)
*Paste in the copied url*

After a short time Excel will display a preview of the table structure, if you are happy with the preview you can go ahead and click _Load_, alternatively you can click _Transform_ to make refinements to the ingestion such as specifying that the first row should be treated as headers (Excel doesn't always infer this) or setting the data format of one or more columns before proceeding with the ingestion.
![Excel - Preview Data Format](assets/excel-data-format.png)
*Preview the Data Format before proceeding*

Once you have done this Excel will create a new sheet containing your WorkfloPlus data.
![Excel - View Imported Data](assets/excel-imported-data.png)
*View the imported Data*

### 4. Manage the Query
#### Refresh
To refresh the data set to include the latest jobs click refresh within either the Data, Table Design or Query ribbon.
![Excel - Refresh Data](assets/excel-refresh-data.png)
*Refresh the data*

#### Query Details
To view the details of the query click on the query in the Queries & Connections panel.
![Excel - Query Details](assets/excel-query-details.png)
*View Query details*

### A note on Power BI
The approach above leverages Microsoft's Power Query which is shared by both Excel and Power BI and therefore the method for ingesting data to Power BI is similar to that for Excel.  
_More to come on Power BI soon_