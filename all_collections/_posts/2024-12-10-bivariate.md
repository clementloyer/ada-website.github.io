---
layout: post
title: "Bivariate Analysis"
date: 2024-12-10
categories: ["Data story", "Milestone 3"]
---

### How do budget and revenue behave ?
First, to start back where we ended our **univariate analysis**, let's look at our money features : how much does the money invested in a movie (its budget) influence how much it will make (the revenue) ? 

{% include graphs/plot_15.html %}

A correlation exists between movie revenue and budget ! And it is even more important for franchise movies ! That's promising !

Now we might questioned what else could influence the success of franchise movies. 

Let's see if the ratio of the budget over the revenue increases or not throughout the franchise, to have an idea about the return on investment over the years in a franchise : 

{% include graphs/plot_20.html %}

It decreases for the second movie ! Seems like the general opinion was right about second movies ...

### How much are franchise movies appreciated by the public ?

If the return on investment is lower than for the first movie, what about the general opinin ?

{% include graphs/plot_18.html %}
At this stage of the data analysis, the stereotype holds: the average rating tends to drop for the second movie. However, as mentioned earlier, franchise films include several outliers. Let's continue to look at how our features influence their box-office and profitable :

### What are the most profitable genres ? 
{% include graphs/plot_16.html %}

Adventure, Fantasy, Animation, Science Fiction, and Action are the top five most profitable genres. Interestingly, this does not align with the most frequently occurring genres. 

Now, are there some genres where the second movie is more profitable then the first movies ? 

{% include graphs/plot_21.html %}

No, unless for documentary. One can say that the stereotype still increases. 


### Do time metrics influence movie success ? 

One might wonder whether the time between two releases affects revenue or average votes. It seems logical that this gap could trigger nostalgia and, in turn, enhance both factors. However, that’s not the case! There is at least no linear correlation.

{% include graphs/plot_22.html %}



### How well are entire franchises succesful? 

On the other hand the franchise's average vote are correlated with the franchise's profit.
{% include graphs/plot_23.html %}


Several theories could explain the observations made. A franchise likely requires less marketing and communication budget compared to a single movie, as it is already familiar to the public. Additionally, some costs, such as set design or actor fees, might be increased (actors may have contracts for multiple films). And the nostalgia effect would be nice to quantify.

Some further analyses possible would be to add new data giving us merchandise information linked to the movie franchises, as well as the actor/actresses' fame over the years.











