---
layout: post
title: "Biavariate Analysis"
date: 2024-12-10
categories: ["Data story", "Milestone 3"]
---

### How do budget and revenue behave ?
First, to start back where we ended our **univariate analysis**, let's look at our money features : how much does the money invested in a movie (its budget) influence how much it will make (the revenue) ? 

{% include graphs/plot_15.html %}

A correlation exists between movie revenue and budget ! And it is even more important for franchise movies !

Now we might questioned what else could influence the success of franchise movies. 

Let's see if the ratio of the budget over the revenue increases or not throughout the franchise, to have an idea about the return on investment over the years in a franchise : 
{% include graphs/plot_20.html %}

It decreases. Seems like the general opinion was right about second movies ...

### How much are franchise movies appreciated by the public ?


[vote through the sequel 18]
{% include graphs/plot_18.html %}
At this stage of the data analysis, the stereotype holds: the average rating tends to drop for the second movie. However, as mentioned earlier, franchise films include several outliers. So, what could be the recipe to make the best possible sequel?

### What are the most profitable genres ? 
{% include graphs/plot_16.html %}
PLOT "ADJUSTED BOX OFFICE REVENUE BY GENRE" 16

Adventure, Fantasy, Animation, Science Fiction, and Action are the top five most profitable genres. Interestingly, this does not align with the most frequently occurring genres. 

Are their some genres where the second movie is more profitable then the first movies ? 
{% include graphs/plot_21.html %}
[gernes evolution]
No, unless for documentary. One can say that the stereotype still increases. 


**Does** time between movie releases in the same franchise influence its success ? 

One might wonder whether the time between two releases affects revenue or average votes. It seems logical that this gap could trigger nostalgia and, in turn, enhance both factors. However, that’s not the case!
{% include graphs/plot_22.html %}
[PLOT :Box office of a movie and the average vote of a movie vs the year difference between the movies]
To explore further in this analysis, we could compare whether a franchise originates from a well-known book or is linked to the sale of movie-related games, providing a clearer understanding of the potential nostalgia effect.

### How well are entire franchises succesful? 
On the other hand the franchise's average vote are correlated with the franchise's profit.
{% include graphs/plot_23.html %}


Several theories could explain this correlation. A franchise likely requires less marketing and communication budget compared to a single movie, as it is already familiar to the public. Additionally, some costs, such as set design or actor fees, might be reduced (actors may have contracts for multiple films).











