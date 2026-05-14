---
title: Blog 4
date: 2026-05-14
author: Junqi Wu juwu0222
summary: Blog 4
tags:
  - layout
  - interaction
  - UX
---

## Profile Page Layout Adjustment

After completing the backend logic for Messages, I started adjusting the page layout and styling. At first, the content on the My Page page would go beyond the browser window, and the Welcome back section was too large, which pushed the My Listings section outside the screen. So I adjusted the layout so the content would not exceed the page width and height, and I made the Welcome back section smaller. I also made the product cards in My Listings have a consistent height. This way, when users view the items they have posted on the Profile page, they will not be distracted too much by the welcome section.

![Profile page layout](/Deco2017_Blog/assets/images/profile-page-blog4.png)

## Hover Effect

Later, I added hover effects to the product cards in My Listings, the Message buttons inside the product cards, and the cards in the Messages list. When the mouse is placed over them, the cards use `transform: translateY(-2px)`, which gives them a slight floating effect. This makes it easier for users to see which elements are clickable.

## Chat Page Height Issue

At first, the content on the chat page would stretch the page too tall. To solve this once and for all, I changed the chat page so that it adapts to the browser height. The product information stays at the top, the chat area in the middle can scroll, and the Message Input stays fixed at the bottom. This design is closest to the layout of a real chat application.

![Chat page layout](/Deco2017_Blog/assets/images/chat-page-blog4.png)

## Why These Decisions Matter

These frontend adjustments mainly focus on pages that users interact with frequently. If the layout does not match users’ habits, they may be unsure whether a button is used for a certain function, or they may find it difficult to locate a function. So overall, these adjustments make the page look more comfortable, and they also make user interactions more intuitive.