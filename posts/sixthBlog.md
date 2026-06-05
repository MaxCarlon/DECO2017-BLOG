---
title: 6. Reflection
date: 2026-06-04
author: Max Carlon
summary: Assess and reflect
tags:
  - review
  - critique
  - reflect
---

Accessibility

Unfortunately, all the changes I had made to the CSS to address the accessibility issues were not present in the submitted build. This is a massive oversight and also means that it does not reach the W3C accessibility standards - the standout issue being readability and contrast. Lighthouse, WAVE and axe DevTools all identified the many contrast issues across navigation and text elements, particularly where muted colours were placed against similarly coloured backgrounds. Readability is especially important within a social media environment because users are constantly engaging with large amounts of text content.

![WAVE Evaluations](assets/images/reflection_testResults.png)
<br>
<br>

Performance

As established in the previous post, the performance of the website is graded to a high standard. Main optimisations would include locally hosting fonts, combining CSS files, and minifying CSS. These are not particularly significant issues as the project has a relatively lightweight interface, minimal animation, and HTMX-driven partial page updates. As I will explore later in this post, beyond this prototype, there is an opportunity to implement lots of community-related artworks for use in backgrounds, banners, icons and book covers - this will greatly increase the need to optimise and monitor performance.
<br>
<br>

User Experience

I believe that the project creates a clear and intuitive experience that directly adds value to my target community in how they can engage with other people on a social media platform. Overall, the core features greatly support communities where there are multiple entry points, a large body of work or a high risk of spoilers, which the Cosmere is all 3. It allows users to engage with content safely from spoilers. This system is, however, very dependent on the user's actions in order to provide the function it intends to. If a user intentionally or unintentionally creates a post with inaccurate spoiler tags, then the whole system of spoiler filtering hasn’t achieved its goal. This would require moderator oversight beyond user self-moderation to address these issues of posts spoiling others. This is a failure of the system in its inability to enforce validation; however, because post content is abstract and context-dependent, the only viable ways to address this issue are human-acting or AI-driven moderation.
<br>
<br>

Interface

The interface contains large areas of dead space, particularly on large monitors. Additional community integrations, such as quick links to the daily game Cosmeredle or links to the official fan site wiki, would help reduce this issue.

The Coppermind wiki has lots of officially made artwork that could be scraped and used as banners, backgrounds, profile icons, and book covers, which would fill in the dead space with art that is relevant to the community.

The create post button is currently a blue, rounded square with an off-centre white plus - this gives no indication that this is the button to create a post. While users may infer its meaning from other social media conventions, the icon does not clearly communicate its function. This should be updated to more accurately reflect its intended function, either with a clearer icon or text to convey its meaning.

Within the create post page, the spoiler tagging system is unintuitive and messy. All books are simply listed with their name and series in brackets, a better format would be to place the books in order underneath their series as a heading. If someone were to make a post that contains spoilers for the third book of The Stormlight Archive and Warbreaker, they would need to select each Stormlight Archive book and navigate the list to find Warbreaker. A better system would also include the automatic spoiler selection for all previous books to the one that you have selected.

An additional issue with the interface is that the main elements of each page is slightly off center. This is particularly evident on the create post page. This breaks the visual balance of the page and reads as amateurish, which would be detrimental to the bla+bla brand perception. It is a simple fix where the main content should be more in line with the center of the page and the peripheral interactions are placed based on that. On a page like the main feed, it may seem imbalanced with the navigation being further off-center which visually weights the page toward the left side. This would be remedied post prototype with the inclusion of the quick links section and other feature integrations.
<br>
<br>

Functional Requirements

I think I achieved the core functionality and the initial intentions that I had identified early in the project. There is a functioning tagging system where users apply tags to their profiles and to posts that they make, and then posts are accurately filtered based on those tags. There is also persistent posts, likes and comments. Manual testing of account switching, spoiler filtering, and direct URL access generally showed the core systems behaving consistently.

With those points, I achieved the core of the brief; I would not say that I achieved my initial vision. While the underlying logic is functional, the presentation feels underdeveloped. As mentioned in the interface section, there is a lot of value in a simple information hierarchy that isn’t being utilised in post-spoiler selection. The lack of artwork, in particular for the book covers, I think, not only makes the visual presentation of the website fall short but also hinders reaching the culture of the community. The Cosmere is an extensive series, so the use of good information organisation is important. The Cosmere is also a visually rich fantasy series that contrasts poorly with an overly minimal interface.

Earlier in the development process, I placed greater emphasis on profile customisation; however, through implementation, I realised that the spoiler filtering and information organisation were significantly more important to the user experience and addressing the bespoke feature of the brief. In addition, something like profile icons would be heavily tied to scraping images off the Coppermind wiki, which is linked to the book cover feature that I had already decided not to pursue.
<br>
<br>

Lessons Learned

Coming into the project with limited technical knowledge, a lot of my effort was placed in keeping up with the tech stack and how to write code. I found myself in a conundrum where if I didn’t use an AI-assisted workflow, then I wouldn’t be able to develop my ability to design around the brief criteria, but if I did use an AI-assisted workflow, I wouldn’t be strengthening my ability to develop with the tech stack. Now that I am at the end of the process, I understand and accept that my coding ability is not strong enough to create this project without assistance, but I have developed a greater understanding of the pipeline and the purposes of each tool in the tech stack. With my current understanding, I would’ve used AI-assisted implementation earlier to rapidly prototype systems beyond my current programming ability, so I could focus on evaluations, debugging, iterative refinement, and understanding the intentions of the brief and web development process. I believe that the original scope I had set out was appropriate, and I could’ve reached a better final product had I embraced the use of AI. I am confident in my decision to make a modular system structure that connects series to books, then books to accounts and posts, and accounts to posts. With this structure, it is easy to scale when new books are added to a series without the core spoiler filtering system breaking, with the only pitfall being the additional need for admins/moderators.