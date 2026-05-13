---
title: Blog 2
date: 2026-05-13
author: Junqi Wu juwu0222
summary: Blog 2
tags:
  - database
  - DBML
  - DDD
---

## DDD and DBML Design

After completing the wireframes for the Messages page and the Profile page, I started designing the database for that part of the project.

At the beginning, my group member created a basic version of the DBML. Based on that, I standardised the naming and added the conversation-related structure, so that the system could simulate chats between buyers and sellers.

Why I Added Conversations

At first, I also considered using only the message table to implement conversations, because each message already has sender_id, receiver_id, and product_id. This looked simpler and would also require less code.

However, when I was actually building the Messages feature, I found that the message list needs to display a complete conversation thread, not a single message. For example, the same buyer can ask about both IKEA Desk and Kettle at the same time. If I only used the message table and made temporary checks, it would be easy to click Kettle but accidentally enter the Desk conversation. From the seller’s perspective, it would also become complicated, because the seller needs to see who has asked about a specific item.

So I added conversations to represent “a conversation between two users under a specific product”, while message is responsible for storing the actual chat messages. This makes the logic clearer and easier to maintain.

## Main Entities

Entity | Description
users | Stores the basic login users provided by the template
user_profiles | Stores the user profile information displayed on the page, such as name, email, university, and avatar
category | Stores product categories
product | Stores second-hand item information
conversations | Stores the conversation thread between two users under one product
message | Stores each individual chat message
