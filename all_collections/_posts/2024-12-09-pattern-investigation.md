---
layout: post
title: "Pattern Investigation"
date: 2024-12-09
categories: ["Data story", "Milestone 3"]
---
Franchise can be really different from one another, most of them are pretty classic with around 3-4 movies and last around 8 years as seen in univariate part and some can be really special like the James Bond franchise, which is around 25 movies that lasted over 45 years and that has a high average revenue. We also have re-makes that are still considered a franchise of two movies spaced by more than 15 years. This is a reason that makes it hard to really see how the franchise behaves. In an attempt to make this more clean, we clustered the franchise with the _k-nearest neighbors algorithm_, let’s have a look at the results:

{% include graphs/franchise_clusters.html %}

One of the main behaviour of budget and revenue is still present here, higher revenue franchise have a higher budget.

To get an idea of how the cluster were made, the genre is the most clear one to understand which cluster represents what type of franchises. It looks like the genre was the features that have a lot of impact on the algorithm. Looking at both the results and the collections in each cluster, we were able to give a general name for each cluster:

---
**Cluster 1:**
It's mainly composed of musical franchise, the combination of the `music` and `drama`, looking at the franchise also helps. It is also a minority in the dataset.

**Cluster 2:**
This is one of the first really big cluster, it looks like its mostly teenage movies, animated movies, Disneys and family sitcom. The main genre is `comedy`, `family` and `adventure`.

**Cluster 3:**
Also a big cluster, it is mainly composed of `action` movies that requires a higher budget to be produced and

**Cluster 4:**
Here the main genre is `horror` and `thriller`; this combination makes it really clear what type of movie this is about. A noticeable feature of those franchise is their remarkably low average budgets, this help maximizing their potential to achieve an outstanding revenue-to-budget ratio.

---

There are a few other interesting things to notice, first most of the franchise kind of perform the same in terms of ratio across every genre and budget. The thing that differentiate a franchise that performs well from one that performs really well is a outlier behaviour that with this dataset cannot be explained clearly. 

However, something is still missing, we see that the general behaviour of franchise successfulness  varies a lot but we have no info yet on the success inside a franchise between the different movies in a franchise. That's why in the next part we're going to look deeper at the interaction between the first a second and: 
> When a movie is successful, wanting to continue the story is always tempting; but how do we make a second successful movie, or even eventually, a successful franchise?


A similar clusterings method was used but now to group common feature of both the first and second movies. In order to make it more interppretable and have better insight of common behaviour the dataset was separated in two main category:
- The franchises were the first movie has a better ratio than the second one, they were assign a positive cluster number
- The franchises were the second movie has a bettwe ratio, they were asign a stricly negative cluster number

Here are the results of the clustering:


First, there's still common behavious that budget and revenue are corelated, we also observe that we have different range of budget/revenue separated. The genre feature still has a strong impact on the clusterisatiton too.

Another interesting fact is about the ratio. Since we grouped the franchise, a common behaviour for franchise with a increase ratio is that a decrease of budget was done and vis ver ca.

**Cluster -3:**
First Cluster where the ratio has improved, it is mainly high budget movies that didn't got a significant increase of budget for the second movie but performed even better, the vote average didnt change. It has a main genre of `Action` and `Adventure`.

**Cluster -2:**
This is a really interesting cluster, it looks like a part of those second movie were not really apriciated even tho it got a increased in revenue from the first movie, maybe the fame of the first movie was used to create a lowered budget one to make a second movie ? Note that its mainly comedy, drama and romance, which can also sometime be genre that are harder to make a second story.

**Cluster -1:**
This is similar cluster to the cluster -3 but with lower budget and revenue

**Cluster 1:**
First cluster where the second movie ratio is worse,