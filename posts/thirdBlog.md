---
title: 3. Wireframe breakdowns
date: 2026-05-01
author: Max Carlon
summary: Wireframe annotations and critique
tags:
  - wireframes
  - UX UI
  - interface
---

Home Page

![Home wireframe](assets/images/wireframeHome.png)

I decided to follow a more traditional social media layout
- profile circle icon, in the top right
- Large home icon centered in nav bar
- Posts follow conventional 'card' layout
  - Title -> Body -> Like / Comment / Share
- Main content kept in middle third of screen
- Ininite scroll on content

My reasoning
- Cosmere community is predominately on reddit and their own forum website 17thshard.com
  - Accessibility and familiarity with reddit systems, married with the focused culture of 17th Shard
    - Unique experience because 17th shards community interaction is a little hidden and reddit doesn't have features bespoke to the community
  - I want systems that are simple and familiar
- Infinite scroll is a more direct way of engaging with content that is often presented in a forum-style format
  - Offers more context of what content is in each post visually - forum posts there is an additional step of clicking into them to understand what is it about
  - It does have performance cost issues -> render posts in increments and not all at once

Non-standard
- I have the primary navigation as a column on the right of the page
  - Keeps navigation closer to area of interest (infinite scroll card section)
    - Key value of navigation and information
  - I can have that navigation be consistent on the profile page
  - I had lots of whitespace on the screen and I wanted to fill it in to make it look less empty



Profile Page

![Profile wireframe](assets/images/wireframeProfile.png)

I want to keep this page very simple. To get the minimum viable product there isn't a lot that needs to be added to the profile page. I just need the one big bookcase feature.
- Consistent side bar navigation
- Primarily focused on bookcase
  - The feature that makes the web app work
- Bookcase resembles a bookcase (the one at bookstores with cover out) / dvd display / item carousel (netflix, online shopping, etc.)
  - Turns tagging system into a visual presentation
    - Showcase your identity and personality -> user builds connection with service
- Bookcase organised by series then book -> clean information hierarchy
- Takes the personalised experience (Bookcase display), uses data to inform a personalised experience (User context post interactions)

Notes / Critiques
- I haven't presented how to add books to bookcase
  - Where is the button to add book? Do books always show and then you select the ones you have read, then they becomde highlighted?
  - How am I getting the bookcovers for the books in the bookcase?
    - Could use wiki image scraper
- I have shown a profile icon but not addressed how to change the icon or what you can change it to
  - I think I would prefer to scrape images off "coppermind" and have those be options
    - Similar to profile icons on Netflix or Nintendo - select from offered icons
- I think both these aforementioned points are valid, however in the interest of the prototype I can cut the profile images and put the bookcovers on the backburner.



![Post wireframe](assets/images/wireframePost.png)

Post Making

Again I wanted to keep a relatively basic design, but I found it challenging where and how to incorporate the post tagging feature.
- Clear structure - Title box, body box, x exit top right, post button bottom right
  - If I am adding additional and unfamiliar elements, the base should be simple and familiar
- Drop down menu to open and select spoiler tags
  - For such a key feature I don't think it should be hidden away and potentially forgotten by the user

- Top row variation - displays arcs/eras within the series and the books within them
  - Doesn't scale well when selecting multiple series
  - Requires too much space to visually work
  - Not intuitive for auto selecting after a certain book

- Bottom row variation - each series has a drop down of books in chronological order
  - Visually cluttered - lots of text and selection boxes with little space to breathe
  - Uses lots of vertical space - and unevenly because each series has a different amount of books

- Neither option has room for additional series
- System is still very dependent on user discretion and knowledge
  - There are characters and events late in one series that spoil early books of another series
