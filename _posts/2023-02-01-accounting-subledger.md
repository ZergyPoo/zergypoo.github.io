---
layout: post
title: Accounting Subledger
subtitle: Transforming Accounting Data
author: Evan Kennedy
---

Customers often have much of their data scattered around their Salesforce organizations. Accounting Subledger (ASL) is a tool that gathers this information and flattens it into a format that most accounting software can ingest.

Furthermore, ASL allows customers to customize and define where their data is, so that it's not proscribed for them. 

## My Role

Co-lead developer. I built much of the generation tools and UI for this project.

## How was it built?

Using a Lightning Web Component (LWC) front-end, we built the interface to let customers tell us where their data resides. It shows them all the objects, custom or standard, in their org, then shows them the fields on those objects that are compatible with the accounting data output. 

Once they have done this, ASL generates a Data Processing Engine definition to transform this data on a scheduled basis. It is capable of transforming tens of millions of records within a matter of hours.