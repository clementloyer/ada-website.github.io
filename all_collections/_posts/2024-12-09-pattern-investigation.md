---
layout: post
title: "Pattern Investigation"
date: 2024-12-09
categories: ["Data story", "Milestone 3"]
---
Franchise can be really different from one another, most of them are pretty classic with around 3-4 movies and last around 8 years as seen in univariate part and some can be really special like the James Bond franchise, which is around 25 movies that lasted over 45 years and that has a high average revenue. We also have re-makes that are still considered a franchise of two movies spaced by more than 15 years. This is a reason that makes it hard to really see how the franchise behaves. In an attempt to make this more clean, we clustered the franchise with the k-nearest neighbors algorithm, let’s have a look at the results:

      {% include graphs/franchise_clusters.html %}

To get an idea of how the cluster were made, the genre is the most clear one to understand which cluster represents what type of franchises. It looks like the genre was the features that have a lot of impact on the algorithm. Looking at both the results and the collections in each cluster, we were able to give a general name for each cluster:

Cluster 1:

It's mainly composed of musical franchise, the combination of the music and drama, looking at the franchise also helps. It is also a minority in the dataset.

Cluster 2: 

This is one of the first really big cluster, it looks like its mostly teenage movies, animated movies, Disneys and family sitcom. The main genre is comedy, family and adventure.

Cluster 3:

Also a big cluster, it is mainly composed of action movies that requires a higher budget to be produced and

Cluster 4:

Here the main genre is horror and thriller; this combination makes it really clear what type of movie this is about. A noticeable feature of those franchise is their remarkably low average budgets, this help maximizing their potential to achieve an outstanding revenue-to-budget ratio.


There are a few other interesting things to notice, first most of the franchise kind of perform the same in terms of ratio across every genre and budget. The thing that differentiate a franchise that performs well from one that performs really well is a outlier behaviour that with this dataset cannot be explained clearly. 

However, something is still missing, okey we can see that a franchise successfulness can vary a lot but the success inside the different movies in a franchise can too. That's why in the next part we're going to look at the interaction between the first a second and how from a first movie that works wanting to make a following one is always tempting but how to make another successful movie or a successful franchise?

The same clusterings method is used to group franchise with common behaviour in order to identify common patterns.