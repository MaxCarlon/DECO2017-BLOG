---
title: Breaking the brief
date: 2026-04-16
author: Max Carlon
summary: What are the key elements from the brief?
tags:
  - tag1
  - tag2
  - tag3
---
What are some thing from the brief that I think are important to keep in mind during this design process? Why and in what way are these things valued? 

- Community Hub
- No sign up page
- Key in on information and its curation
  - Information and Experience
  - Something beyond subreddit/facebook group

  Standards
- AA accessibiity or higher
  - accessiblity starts in the ideation process - be sure not to add as after thought
- EU cookie and tracking policies
- Responsive for Desktop and Mobile
  - Pick one as default focus
- Use prototype template (the project and tools provided)
- Git version control
- Load time less than 1 second, never more than 3 seconds

  Other Tech notes
- Session token stored as cookie
- Routes can inspect cookie and user ID and username
 - Page can apply username from the stash (no database)
- Web app should be adaptive to user
  - I want to avoid making things static

  Keystone feature
  Unique / Standout / Bespoke   Feature
- Each user profile experience should be unique
- Relevant to the community you are designing for
- Should tie in to BlaBla values - information and experience
 - how someone navigates, what information they see, how they post, what they can post/share, how community interaction happens, 

  Communities that I am familiar with
- anime, gaming, photography, 3D art, gamedev, NRL, daily games, cosmere, books, fantasy
  - ones I might want to think more on - cosmere and deadlock

Breaking down the notes
Key Functions
- Community Hub
  - Must be centered around shared interest and interaction beyond posting
    - Drives engagement and aligns with BlaBla's value of information and experience
    - Features must enable connection, content display is not enough

- Information Curation
  - Users see relevant and filtered content catered to them
    - Reduces content noise -> members build connection - "Curating the right experience is what keeps them coming back."
    - Requires emphasis on the quality of filters and tagging. Large logic workload - what is the performance cost?.

Technical
- Accessibility
  - Must influence layout, contrast, navigation from the start
  - Can easily be forgotten or missed for implementation

- Performance
  - Limits scale and size of data manipulation
  - Be specific in what data is called or refreshed

- Responsive Design
  - Responsive for user experience and for device display
  - Sacrifice visual fidelity for better functionality

Bespoke Feature
- Change how users interact, not just what they see
- Community-specific
- Directly affect information + experience

- My direction
  - Personalised filtering/tags
  - User-specific feed behaviour
  - Context aware posts (what users can see)