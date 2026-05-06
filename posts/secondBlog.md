---
title: Community Exploration
date: 2026-04-17
author: Max Carlon
summary: Two communities and their potential design directions. Further exploration of chosen community. 
tags:
  - tag1
  - tag2
  - tag3
---
 Two community options breakdown
Deadlock
- can use pre-existing APIs
  - already accessible resource
  - wide pool of relevant information
  - data can enable unique experiences per user
  - already a few (non community focused) websites that use this API
- Harder to implement social / community aspect
  - Would boil down to a merging of the subreddit and account tracking websites
- Is probably a larger scrope
Cosmere
- data required for unique experience is less and more relevant
  - most relevant information breaks down to Series -> Books -> Worlds (maybe some other lore relevant information)
    - Simplest breakdown of required filters to see relevant user content and avoid spoilers
- far more achievable minimum viable product
  - ends up just working with tags on accounts and checking them against posts tags
- more relevant integrations for community 
  - cosmeredle, knight radiant quiz
    - I don't think there is a way to actually integrate these though
      - could be a part of a "links hub" to other websites that are relevant - like the wiki

_______________

After talking with Sam I think the cosmere option is the one I should pick. It should be less dificult to get the main feature implemented. I can also probably fit another feature or more user customisation.

_______________

Chosen Community - Cosmere
- More feasible product - simple data model
  - Series -> Books -> Tags
- Less complex implementation compared to Deadlock API
- Stong alignment with bespoke feature requirements - spoiler filtering
- Better basis for community interaction
  - Theories, discussions, fan art, etc.
- Requires constructing data/content instead of relying on premade

Cosmere Core Feature
Spoiler tag/filter system
- User selects books they have read
- Posts are tagged by book/series relevance
- System filters out posts related to books that the user hasn't read

- Improves user expreience (avoid spoilers)
- Creates a safe place for users to engage in = encourages engagement
- Meets information curation target

- Requires users to be consistent with tagging
  - Potential need for moderation
- Very negative user experience if filtering is incorrect (they get spoiled)

Minimum Features Feasability
- User account book tags
- Post spoiler book tags
- Filtering posts against accounts

Implementation of features
Core
- Bookshelf - tracks read books
- Post tagging system
- Filtered feed

Achievable Stretch
- Series specific tabs
- Links to other community relevant websites

Most likely not achievable
- Lore-based UI naming - Alternative titles and names to base
- Interactivity from community websites - quizz results affects profile

Cosmere and web app questions / exploration
What I need to find out about Cosmere fans
- How do they interact online (what websites, what is the culture)
- What do they talk about (is it mostly fanart? theories? fanfic?)

Where are posts made? On your profile? On a major posts page?
- Is there a major posts page called Silverlight (lore tie in)? Do you world-hop to filter posts by series relevance? If someone has only read one book should it be called Silverlight/Shadesmar/Cognitive Realm - have a lore relevant tie in at the risk of potential spoiler references?

How are you selecting the relevant subpages and also selecting spoiler tags?
- You can have relevant series top selection and then select the book up to where it doesn't spoil - Every book selected after is automatically selected 

![alt text](../assets/images/postDraft.png)

Where do I want the default homepage to be?
- Silverlight (the all posts page) - user directly enters where they can see the most content
- Seperate landing page - user can decide to go to specific forums here, user feels like they have more control over what they see/where they travel 
  - least likes idea - adds a whole new page that I would have to fill out and seperates users from directly entering to where the content is
- Account page - same idea as landing page but it is their "home" that they travel out of


![alt text](../assets/images/webpageDraft.png)
