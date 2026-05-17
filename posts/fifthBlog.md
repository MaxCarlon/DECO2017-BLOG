---
title: 5. Implementation and Ai
date: 2026-05-17
author: Max Carlon
summary: Using LLMs to create the website
tags:
  - tag1
  - tag2
  - tag3
---

To account for my lack in technical skill, I decided to implement LLMs into my development process. This rapidly increased the speed at which the prototype could be iterated and allowed me to focus more heavily on the major design elements and user experience decisions. However, this also meant I needed to run additional testing and error checking to ensure that the generated code functioned correctly and accurately met the project brief.

To start, I provided ChatGPT with my study notes, blog posts, brief and rubric so it can understand the requirements of the project. This includes - 
- the tech stack 
- database logic 
- accessibility and performance requirements
- the bespoke community specific feature.

I then asked ChatGPT to generate an overarching implementation prompt to give to OpenCode. This covered - 
- required pages
- routes
- database tables
- htmx interactions
- session behaviour
- accessibility requirements
- responsive design requirements
- spoiler filtering logic
- seed data requirements

After this first implementation pass, I began running some tests.
Filtering system tests
- I created a new account and confirmed that only non-spoiler posts were visible.
- After adding books to the user bookshelf, posts with the corresponding spoiler tags became visible.
- I also attempted to directly access spoiler posts via URL. The system correctly prevented access unless the account had the required tags.
Persistence tests
- I created posts, comments, and likes on one profile.
- After switching to another account, all authored content and interactions correctly persisted within the database.

Issues I encountered
- Clicking "create post" with empty fields correctly produced an error to the user. However, no error occurred when each field was full of spaces - it didn't post but there was no error.
  - After several iterations the issue was resolved
- The bookshelf was illogically organised - books were not sorted by series and chronological order, several books were missing, a book that didn't exist was in the data.
  - I decided to tackle this issue after I addressed some major UI/UX issues

I then moved to UI and UX iteration by supplying screenshots of my wireframes to inform my prompts to OpenCode.
Home changes
- series navigation converted into tab-style navigation
- “create post” changed into a floating action button
- profile access moved to the top-right corner

Profile changes
- restructured bookshelf into shelf/carousel sections
- added placeholder book covers
- reorganised Cosmere books into accurate series groupings
- adjusted seed data to better reflect the Cosmere universe

At this point, the prototype appeared mostly functional from a surface-level overview. The core systems were operating correctly and the application visually resembled the intended final design. However, further testing and additional validation is still required to ensure the website is genuinely meeting the project requirements and isn't simulating functionality.

WCAG Accessibility & Testing
![accessibility test results](assets/images/accessTestResults.png)
From these tests, I identified significant contrast issues that can be resolved by adjusting CSS colour values and link styling. Lighthouse also identified loading delays caused by Google Fonts requests. For the prototype, I believe it is appropriate to use default system fonts to reduce loading and improve performance.

Mechanical testing
Mechanical testing is still required before the final prototype submission. While the major systems appear functional through manual testing, I have not yet implemented formal integration or automated testing. Since much of the implementation was generated and iterated with AI, additional testing is important to ensure the application is genuinely performing the required logic rather than only appearing functional at a surface level.