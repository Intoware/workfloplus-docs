---
layout: page
title: Zapier Introduction
permalink: /zapierintroduction
nav_order: 12
---

Beta
{: .label .label-yellow}

_N.B. Our Zapier App for WorkfloPlus is still in Beta, if you are interested in being part of the Beta programme or just finding out more please contact us at <support@intoware.com>._

## Introduction to Zapier
Zapier is an automation tool that allows users to define connections between applications, automating the flow of data from one application to another. There are several tools in this space, including some interesting new challengers but Zapier is recognised as the market leader.

![WorkfloPlus Zapier](assets/workfloplus-zapier.png)
### How does Zapier work?
Zapier is a web application that includes both free and paid-for tiers, users can create and manage their own automation workflows known as "Zaps" by connecting together "Apps", there are hundreds of different Apps supporting different actions and connections into different tools.

### Why have we made a WorkfloPlus app for Zapier?
It is possible to achieve a lot of the integration functionality this documentation will cover without the WorkfloPlus App, by using the generic Apps for HTTP requests and JSON parsing, however the WorkfloPlus App makes selecting the relevant data much more straightforward.

## Getting started with Zapier
Zapier's documentation covers all the fundamentals for getting started, learning the basics is recommended before getting started; this page covers [creating a Zap](https://zapier.com/help/create/basics/create-zaps)

## Example 1: Writing Job Data to Google Sheets
In this example a Zap is created to select data from completed Jobs (for a specified Workflow) and then write that data to a Google Sheet.

Firstly create a new Zap and select the WorkfloPlus App for the first stage, confirm the Trigger Event is "New Completed Job" (this means the Zap will run every time a new Job is detected) and then press "Continue".
![Zapier 1_1](assets/zapier-1-1.png)
![Zapier 1_2](assets/zapier-1-2.png)

Next sign-in to and connect to your WorkfloPlus account.
![Zapier 1_3](assets/zapier-1-3.png)

Now select the Workflow from the drop-down, in this case we can set the Standard Report option to false