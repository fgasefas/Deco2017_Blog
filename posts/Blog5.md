---
title: Blog 5
date: 2026-05-14
author: Junqi Wu juwu0222
summary: Blog 5
tags:
  - dispute
  - refund
  - prototype
  - scope
---

## Refining the Scope of Transaction Protection

At the beginning, when I designed this platform, I wanted it to be a second-hand trading hub for Chinese international students in Australia. I wanted it to solve the trust issues that Chinese international students often face in Australia when moving house or trading second-hand unused items. This is because when many students trade on social media platforms, they basically rely on both sides messaging and negotiating with each other, without a fair third party to organize the transaction. This can easily lead to disputes.

## Simulating Refund and Responsibility Decisions

However, at the current stage, real backend fund holding, payment accounts, and customer support cannot truly be implemented because of technical limitations. So my plan is to make the payment transaction and customer support into a feature that can be simulated. In other words, what the user sees is a complete second-hand transaction process, but the system behind it does not actually handle money. Instead, it follows preset steps to simulate transaction statuses such as “buyer has paid,” “seller has shipped,” “buyer has received the item,” and “buyer has requested a refund.”

Also, the platform rules need to be considered. For example, if the buyer has already paid but the seller has not shipped the item yet, the system can suggest that the seller refund the buyer. If the seller has already shipped the item and the buyer requests a refund, then if there is no quality issue, the system should not suggest continuing with the refund. All rules should be based on fairness and justice.

## Data and Flow

To implement this feature, we could later add a transaction-related data structure to store the item, buyer, seller, transaction status, refund request reason, and results such as the platform’s decision. The user flow could be that the buyer and seller first chat around the item. After confirming the transaction, they enter the transaction page and update the transaction status. If the transaction goes smoothly, the transaction ends. If there is a problem, the buyer can request a refund, and the system displays a simulated responsibility decision based on the current status.

## Reflection on Feasibility

This practice also made me realize that when developing the community platform, I cannot just add whatever feature I want directly into it. Before adding a feature, I need to think about whether it will affect the existing pages and code logic. For example, the product, user, messages, and profile pages have already been completed. If I add the transaction flow later, I need to consider which product it is connected to, who the buyer and seller are, and whether the product status needs to change after the transaction is completed.