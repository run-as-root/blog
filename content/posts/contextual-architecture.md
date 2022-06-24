---
title: Contextual Software Architecture 
author: David Lambauer
date: 22.07.2022 
draft: false
keywords: prologue, run_as_root, homepage
description: run_as_root Project Documentation 
---

## Contextual Software Architecture

There are dozens of books and other reading around the topic of software architecture. Historical classics like the
”Design Patterns. Elements of Reusable Object-Oriented Software” by the “Gang of 4”, for example, belong in every
well-sorted home library. Software architectures or design patterns are intended to help solve recurring problems
logically. The difference between the examples in the books and the code that is developed in practice can be enormous.

One then wonders about code that is difficult to understand and maintain. Not to mention further development and
extending it. The difference between theory and practice is, in my opinion, the lack of context. Understanding the
context of a development is crucial in order to be able to correctly classify the respective software. Developing a
proof of concept with a single developer has different criteria for the underlying software architecture than long-term
maintenance and further development of an eCommerce system. Ask yourself the question:

Am I developing for the free market or for a government? Am I creating components in a framework or just using it?

We are an eCommerce agency with a focus on Magento. Many of our clients use Magento. Some of our stores have 100 orders
an hour, others only five a day. Some customers make their sales during a certain season, others stretched over the
whole year. When we talk about implementing new features in the team, and when it comes to creating a technical concept,
I often hear phrases like, “It’s done the same way in Magento Core,” “This is Magento standard,” or “This is how it’s
most flexible.” Again, the context is missing. Regardless of the evaluation of Magento Core’s quality, we as a service
provider have a different focus and goal. Magento, seen as a framework, must be flexible enough, to be able to handle as
many different use cases as possible. Code in the core must remain backwards compatible. Developers working with Magento
must be able to extend the core accordingly. All this counts only conditionally for our work. Our goals are to cover the
requirements of our customer and to keep the system simple and comprehensible, so that the maintainability is preserved.
Depending on the customer we develop a product import as a simple cron or asynchronous with message queues. In addition,
the person who wrote the code is often not the person who fixes the code when there is a bug.

So how do you manage to structure your code in such a way that it not only meets the business requirements, but also the
requirements you have for it (maintainability, extensibility, easy to understand for others, …)? The answer can only be:
It depends. You must be able to clearly formulate the requirements for your own code. There is certainly always a
balance of power. If I want to develop new features as fast as possible, maintainability probably suffers. If I always
develop alone, I probably lose the ability to write code so that others can easily understand it. Software architecture
or design patterns help us in theory to solve problems or to structure our project. However, it should always be
questioned whether the pattern in the book also fits my particular context. Furthermore, it is always good to question
the old familiar patterns, such as in the book of the Gang of 4 in general. After all, the book was published in 1994.
Is it still relevant at all?