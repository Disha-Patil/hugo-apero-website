---
author: dp
categories:
- ML
- RecSys
- R
- Algorithm
date: "2017-01-31"
draft: false
excerpt: Demystifying the recommendations seen on various sites. This post is aimed at curious folks from non-ML background.
layout: single-sidebar
subtitle: 
title: So what's behind amazon recommendations?
---

__“Watch Elementary if you love Sherlock”__

__“You love stationary? Check out these cool and colourful sticky notes ”__

We give (and receive) such suggestions in our daily life to the people whom we know well or at times to people we don't know so well but have surest information of their particular interest. We make an useful suggestion based on the information available to us. It may or may not work always (how well do you know your friend?!)

Now consider a computerized method trying to study your behavioural patterns depending upon your online activities, some personal information provided by you, and then recommending a set of things you might be interested in. That is what is called a Recommendation System / Engine / Platform. Choose what you might like to call it, but it is exactly what amazon uses that makes that beautiful cyan bottle lamp you added to wishlist last week follow you everywhere (until you loose interest or at last buy it!)

### To put in some formal definitions:

Recommendation System (RS) refers to computerized method to predict an user's preference for a certain item. Recommender Systems (RSs) are software tools and techniques providing suggestions for items to be of use to a user.

Typically, a RS will provide an user with a list of suggestions/recommendations based on various characteristics of the users and items. “Items” is what is being recommended by the system. “User” is to whom the item is being recommended to. Characteristics of items is the set of metadata of each data item. “Characteristics” of users is contextual and can be classified into explicit and implicit measures. Definitions can be better understood with an example.

#### Example:

An online book recommendation system. The item to be recommended here is a book. User will be registered or not registered on the online platform. It is difficult to produce a personalized recommendation list for unregistered users because no explicit information about the user is available. Lets say an user is registered on th online platform. The personal information about the user's likes and preferences is used as the explicit information by the RS. In addition to this, by various measures a set of implicit information is extracted and attributed to user's characteristics. For e.g. amount of time spent by the user on certain product/item page, item views by the user, items favourited/shortlisted by the users, etc make up for implicit information about the user. The item-book- has set of identified characteristics, for e.g., author, time of release, genre, language, average ratings by users etc.

Before we go into how the RS works, lets try to understand why the need for RS?

Primary concern for users is to be able to weed through this vastness of available options in the world for anything you wish to have/watch/read etc. Primary concern for service providers is to increase sales.

###  Recommendation Systems : value for users and for service providers


	
| Value for Users               | Value for Service Providers               |
|-------------------------------|-------------------------------------------|
| Discover new things           | Increase sales                            |
| Explore options               | Opportunity for promotion of new items    |
| Narrow down the set of choices| Obtain more knowledge about the customer  |
| Find interesting things       | Increase customer loyalty and build trust |



About discovering new things and goal of RS :

What is the advantage of an online store over a physical one?

Ans: physical stores have space constraints and hence resources are limited. Online stores have huge advantage over physical stores on this front.

The distinction between the physical and online worlds has been called the long tail phenomenon,fig(1). The vertical axis represents popularity (the number of times an item is chosen). The items are ordered on the horizontal axis according to their popularity. Physical institutions provide only the most popular items to the left of the vertical line, while the corresponding on-line institutions provide the entire range of items: the tail as well as the popular items.

The goal of recommendation system is to beat the popularity metric (number of ratings, average ratings)

Example :

Amazon recommendations made a forgotten book into a best seller almost a decade later. “Touching the void” (1988) rose to be best sellers because many people searching about “Into thin air” (2002) were also searching for the former.

How does recommendation system work?

Recommendation system helps to match users and items. Given an user or user model (e.g. ratings, preferences, demographics, situational context, behavioural patterns) and items (with or without characteristics) RS finds relevant score by which the items are ranked and finally a relevant list of recommendation is given.

Keyword here is “relevant” and relevance is context dependent. Also we are interested in the characteristics of the list. e.g. how diverse is the list? (what new does the user discover if he/she is shown only similar items)

A matrix containing user-item pairs and a value know as degree of preference is called a Utility matrix. This matrix is a sparse matrix, meaning most of the entries are unknown. The goal of a recommendation system is to predict the blanks in the utility matrix.[2]

Paradigms in Recommendation System :

1. Personalized : based on user profile and contextual parameters (explicit and implicit parameters)

2. Collaborative : based on community data (“what do my friends like?”)

3. Content based : based on features of the product/item (“show me more of what I so far liked”)

4. Knowledge based : based on best information about users needs (“what is the best fir for my needs?”)

5. Hybrid : combination of various inputs and compositions of different mechanisms

Evaluation of recommendation systems :

Evaluation is required at different stages of the systems life cycle for various purposes.

1. Design phase

off line evaluation is carried out in this phase. The goal is to verify appropriate approach. Several algorithms run on same dataset and their performance is compared.

2. Online evaluation

The algorithms might be very accurate in solving the core recommendation problem, i.e., predicting user ratings, but for some other reason the system may not be accepted by users, e.g., because the performance of the system is not as expected. At this stage it is usually beneficial to perform on-line evaluation with real users of the system and analyze system logs in order to enhance system performance.

3. Controlled experiments

A small group of users interacts with various systems and their performances is analyses as well as their experience is recorded via a questionnaire. This kind of evaluation is both quantitative and qualitative.

How do we know these are good recommendations?

Analyze following parameters to evaluate the recommendations-

click through rates, total sales numbers, customer return rates, promotion of certain items, customer satisfaction and loyalty etc.

Can we explain the recommended items?

e.g. “you may like this item because...”

This deals with advance topics in RS and is one of the major research area in this domain. Dealing with explanations in RS is important for service providers because they can now promote item by persuading the users, whereas users can make an informed decision.

(featured image from xkcd.com)