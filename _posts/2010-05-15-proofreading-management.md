---
layout: post
title: Proofreading Management Application
subtitle: Enabling and Managing the Submission of News Articles for Proofreading Review
author: Evan Kennedy
---

At Internet Broadcasting, a company that ran websites for local news stations across the country, they provided a proofreading service for these news articles. Prior to this project, the team had a shared email inbox for these requests, which they would use to manage in a sort of queue. We built a Visualforce, Apex and Integration solution that streamlined this considerably.

## My Role

Lead Developer. I designed and implemented this project in its entirety.

## How was it built?

This was a project that required heavy integration. News reporters would write their stories on the main news site platform, and click a button to submit them to the Salesforce API custom endpoint that I created. This would add the story to the queue, where it could be claimed by the proofreaders. They would be provided a large interfact where they could edit the story in place. Once done, we used a JavaScript library to highlight the differences between the edited copy and the original copy, and notified the reporter via email. This enabled them to grab those changes, or quickly see what they were, and update their story accordingly. 

Some notable problems that I had to solve:

- Collision management, preventing multiple proofreaders from claiming the same story at the same time.
- Email generation and notification.
- API implementation, both the ingesting side, in Salesforce, and the caller side, in the Java application maintained by the company.