---
title: Blog 3
date: 2026-05-13
author: Junqi Wu juwu0222
summary: Blog 3
tags:
  - implementation
  - messages
  - backend
  - frontend
---

## Implementing the Messages Feature

After finishing the DDD and DBML, I turned the Messages page from a wireframe into an interactive page. I needed to make sure that the backend routes, the database, the currently logged-in user, the product ID, and the chat partner could all match correctly.

## Connecting the Page to the Database

First, I connected the Messages page to the database. Then, based on the currently logged-in user, I read data from the `conversations` and `message` tables. The page then displays the conversations related to the current user, together with the product names. In the message list, users can see the most recent chat information.

![Messages list](/Deco2017_Blog/assets/images/messages-list.png)

After this, when a user sends a new message, a new `message` record is added to the database, and the corresponding conversation’s `updated_at` is also updated. This allows the message list to be sorted by the most recent chat time.

## Fixing the Conversation Logic

At first, there was a problem in my conversation logic. When I clicked the Message button for Kettle, it entered the chat for IKEA Desk instead. Also, when the seller viewed their own product, it entered the buyer’s chat page.

Later, I changed the logic so that one conversation must be determined by both the product and the two users at the same time. This means that even under the same product, conversations between different users should be different conversations. If the same two users are talking about different products, those should also be different conversations.

## Chat Interaction

The logic of the chat page is that messages sent by the current user are displayed on the right, and messages sent by the other person are displayed on the left. Each message also shows the sending time. After the user sends a new message, the message is saved into the database and displayed on the page.

![Chat view](/Deco2017_Blog/assets/images/chat-view.png)
