---
layout: post
title: Program Plan Builder
subtitle: A tool to allow advisors to create education programs
author: Evan Kennedy
---

Creating and maging education programs is very difficult. This project, the Program Plan Builder, makes that easier.

Built in Salesforce Ecuation Cloud, it is an LWC that implements the builder framework to help manage and visualize education progrms, such as majors and minors. Rendered in a tree structure, each node represents the program, or a grouping of elective or required courses.

![Program PLan Tree](/assets/img/ppbTree.png)

## Architecture and Organization

The builder uses an subscribe and emit model to broadcast changes across the UI. When the user clicks on a node, the builder emits that node information to the properties panel to render the appropriate form.

![Properties Panel](/assets/img/propertiesPanel.png)

To allow customization, this panel honors the org's page layout properties.

![Form from page layout](/assets/img/pageLayout.png)