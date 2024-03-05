---
layout: post
title: Advisor Link Student Scheduling Wizard
subtitle: Connecting students with their advisors
author: Evan Kennedy
---

A managed package developed on the Force.com platform, Advisor Link has many features. Easily the biggest one of these is the ability for students and advisors to schedule appointments with one another. Enter the student scheduling wizard.

Among many other features, this wizard lets users:

- See who they've recently met with and schedule with them again easily.
- See a list of advisors specifically assigned to them and schedule directly.
- See a list of advising pools, like a generalized financial aid department, and schedule with anyone in the group.

On the advisor side, it let's them customize many elements of the scheduling experience, including:

- Which topics they support.
- How long each appointment is based on which topic.
- The ability to have abailability in different locations and different times.
- The ability to setup appointments that a group of studnets can attend.

## My Role

Lead developer. I architected and facilitated the building of this project.

## How was it built?

The wizard is an LWC component with an Apex back-end. Instead of using a fixed number of pages, it determines what to ask the student next based off of the data they have already selected. If they have selected nothing, it loads the first page, letting them select who they want to meet with. This enabled us to establish a nice, data-driven testing approach, and it also allowed us to facilitate other flows, like the rescheduling of an appointment. Rather than juggle different static pages, we give it the seed data, and it renders the appropriate screen.

![Advisor Select](/assets/img/wizardAdvisorSelect.png)

If they've already selected person/group to meet with, and a topic, the wizard drops them right in the availability selection screen. The slots here are generated using the Advisor's availability settings. Any block they have setup are loaded and divided up into appointment-sized slots. Then, using an interval tree, this availability is cross-referenced with any existing events or appointments they already have scheduled. This is rendered to the user so that they can easily select the time slot that works for them. 

![Availability](/assets/img/wizardAvailability.png)