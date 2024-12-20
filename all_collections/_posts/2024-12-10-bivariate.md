---
layout: post
title: "Biavariate Analysis"
date: 2024-12-10
categories: ["Data story", "Milestone 3"]
---
### How much are franchise movies appreciated by the public?
It is often said that the second movie is not as good, but is that true? What are the average score threw the different movies in a franchise? 

[vote through the sequel 18]

At this stage of the data analysis, the stereotype holds: the average rating tends to drop for the second movie. However, as mentioned earlier, franchise films include several outliers. So, what could be the recipe to make the best possible sequel?

### How do budget and revenue behave?
To keep in mind every values concerning profit, budget, revenue are inflation adjusted. 

As supected before there is a positvie linear regression between revenue and budget that is even greater in franchise movies. 

[PLOT CORRELATION BUDGET _REVENUE]

Now we might questioned what else could influence the success of franchise movies. 

Let's see if the budget and revenue increases or not throughout the franchise : 

[bar chart budget/revenue movie order]

It decreases. The stereotype continues...

The ratio of the revenue over the budget decreases also. 
[plot 20 ]

**What** are the most profitable **genres**? 

PLOT "ADJUSTED BOX OFFICE REVENUE BY GENRE" 16

Adventure, Fantasy, Animation, Science Fiction, and Action are the top five most profitable genres. Interestingly, this does not align with the most frequently occurring genres. 

How about our favorite franchise? Does it follow the analysis? 
Acctually yes! 

**Does** time between movie releases in the same franhcise influence its success ? 

One might wonder whether the time between two releases affects revenue or average votes. It seems logical that this gap could trigger nostalgia and, in turn, enhance both factors. However, that’s not the case!

[PLOT :Box office of a movie and the average vote of a movie vs the year difference between the movies]
To explore further in this analysis, we could compare whether a franchise originates from a well-known book or is linked to the sale of movie-related games, providing a clearer understanding of the potential nostalgia effect.

### How well are entire franchises succesful? 
On the other hand the franchise's average vote are correlated with the franchise's profit.[correlation vote average budget]

Several theories could explain this correlation. A franchise likely requires less marketing and communication budget compared to a single movie, as it is already familiar to the public. Additionally, some costs, such as set design or actor fees, might be reduced (actors may have contracts for multiple films).











