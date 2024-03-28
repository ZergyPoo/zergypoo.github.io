---
layout: post
title: Student Pathway Builder
subtitle: An innovative school career planner for students
author: Evan Kennedy
thumbnail-img: /assets/img/pathwayBuilderThumbnail.png
---

Back when I went to college we would have to pour over the physical course catalogs in order to plan out our school career. We had to figure out which courses were required for our major, what their prerequisites were, and when they were being offered. 

My latest project is the Pathway Builder. A UI that allows students to browse the majors they are enrolled in, which courses are required for them, and enables them to drag and drop courses to each and any of the terms and sessions they are enrolled in. It even allows them to search on the entire course catalog of their school.

![Program PLan Tree](/assets/img/pathwayBuilderOverall.png)

## My Role

Lead developer. I architected and facilitated the building of this project. The entire code organization, pattern and centralized management model were my ideas. 

## How was it Built?

The Pathway Builder is built to be re-usable. The component expects to be provided with data, labels and even functions that represent points of interaction. For our implementation we used a separate data mapper model on the client-side to query for all the data required. We pinged the API to get a list of all the programs the current student is enrolled in, and their planned pathway data as well. The JavaScript code then transforms this into format expected by the builder. 

The Pathway Builder component itself uses a centralized structure for maintaing local data. Every time a new course is dragged into the planned area, the data tree is quickly regenerated with new planned credit hour numbers, so that the UI responsively tells the user how they are progressing toward the completion of their programs. It also maintains an ongoing change state, keeping track of any items that were removed from the plan.

Upon save the builder passes this information into the data layer for parsing. The output is a list of mixed DML comprised of updates, deletions or insertions. 