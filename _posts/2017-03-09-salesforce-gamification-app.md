---
layout: post
title: Gamification App
subtitle: Letting Customers Setup Gamification and Rewards in their Salesforce Org
author: Evan Kennedy
---

A managed package installed in customer orgs, this app provides admins with an interface for setting rules and rewards. It allows the user to select from a list of supported objects, like the Opportunity, dynamically select their fields, and choose thresholds and rewards. For example, when a salesperson closes a deal worth more than $1,000,000 they are awarded a certain number of points.

## My Role

Lead Developer. I designed and implemented this project in its entirety.

## How was it built?

Using apex and visualforce (pre-lightning), I built the interface that let admins select from any object in their org, choose fields, and input field criteria. This supported all data types. 

Then a single trigger able to ingest any object would run, and cross-reference the data, determining if the criteria was met. If so, it would award that person points based off of this data. 

Additionally, this data was synced with a rewards system API so that the user could cash in their points.