---
layout: post
title: Program Plan Builder
subtitle: A tool to allow advisors to create education programs
author: Evan Kennedy
thumbnail-img: /assets/img/ppbTree.png
---

Creating and managing education programs is very difficult. This project, the Program Plan Builder, makes that easier.

Built in Salesforce Education Cloud, it is an LWC that implements the builder framework to help manage and visualize education progrms, such as majors and minors. Rendered in a tree structure, each node represents the program, or a grouping of elective or required courses.

![Program PLan Tree](/assets/img/ppbTree.png)

## My Role

Lead developer. I architected and facilitated the building of this project.

## How was it Built?

The builder uses an subscribe and emit model to broadcast changes across the UI. When the user clicks on a node, the builder emits that node information to the properties panel to render the appropriate content. Similarly, when the user saves their properties, the builder emits the update to the canvas so that it knows to update the tree view.

![Properties Panel](/assets/img/propertiesPanel.png)

To allow customization, this panel honors the org's page layout properties.

![Form from page layout](/assets/img/pageLayout.png)

To enable the easy adding and searching of courses, we created a modal that allows the user to search for, and select, en masse, the courses they wish to add to the node.

![Mass Course Selector](/assets/img/massSelector.png)