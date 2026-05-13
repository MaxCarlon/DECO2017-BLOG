---
title: 4. DDD and ERD pipeline
date: 2026-02-14
author: Max Carlon
summary: Taking the wireframes and identifying key data then defining their relationships
tags:
  - tag1
  - tag2
  - tag3
---


From my wireframes I broke down the key data for the key features I need for the web app to function as intended.

Series
- Series id
- Name -- Name of the series

Books
- Book id
- Title
- Series
- Order -- order of book within series

Users
- User Id
- Username

Posts
- Post Id
- User
- Series
- Title
- Body

From these sets the rest of the functions can be made

Series informs the larger filtering system of posts by what series they belong to. It also organises what books belong to what series, helping with ordering and selecting spoiler tags

Books are linked to the books a user has read and are also used for spoiler tagging on posts.

Users store account information and connect to the books they have read. They are also used for post authorship.

Posts are the driving social functionality. We need post data for attaching spoiler tags to posts and for generic social functions like likes and comments.

![Entity Relationship Diagram](assets/images/ERD.png)
This diagram shows the relationship between the tables more clearly

The key elements of this are the user_read_books and post_spoilers tables. This is where the key functionality happens in the filtering of posts per account. It compares the books attached to a post’s spoiler tags against the books marked as read by the user.
It is also worth noting that they are both join tables. Users can read many books and books can be read by many different users. The same way that a post can spoil many books and each book can appear in the spoiler tags of many posts. These tables make the system more flexible and avoid forcing multiple values into a single field.

Comments and likes are added because they are the core social interaction systems expected within a social media platform. They are relatively lightweight systems to offer interaction.
For the prototype the filtering feature is far more important than all the other interactions that can be had on a social media. That is why I am only implementing the likes and comments and not other features like save or share.

Breaking down the systems into these related tables makes the app easier to scale and maintain. 
Each new series or book does not need to refactor the entire table or relationship diagram. This structure support additional series, advanced filtering, user preference systems or adding new features related to cosmere lore and characters.
It also reduces the need for storing duplicate information on posts or user accounts by using relationships within the database structure.