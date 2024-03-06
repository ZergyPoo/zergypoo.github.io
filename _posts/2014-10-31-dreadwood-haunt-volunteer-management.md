---
layout: post
title: Dreadwood Haunt Volunteer Manager
subtitle: Facilitating the Management of Job, Dates, and Volunteers for a Local Haunted Forest Attraction
author: Evan Kennedy
---

A friend of mine organized a haunted forest in frigid western Wisonsin. A non-profit, Dreadwood relied entirely on volunteers to be run. They ran this out of a series of spreadsheets until this project.

At the end, I delivered a system that:

- Enabled logins for end users to volunteer, signup for dates they were available.
- Enabled logins for coordinators, to login, manage the volunteer lists, check them in, assign them equipment and costumes, and many more.
- Enabled admins the ability to view profiles, view the management screen for a given date, and drag and drop volunteers to the jobs that needed to be filled.

## My Role

Lead Developer. I designed and implemented this project in its entirety.

## How was it built?

As a side project, I ended up building this one in Node.js and hosting it on Heroku with a PostgreSQL database. I designed the entire database of users, volunteers, jobs, and dates. 

I built a series of REST endpoints in the Node.js server-side to surface the data for the application. 

On the front-end I used AngularJS to generate the UI interaction logic.