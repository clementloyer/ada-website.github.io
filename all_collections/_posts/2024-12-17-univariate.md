---
layout: post
title: "Franchised vs. Unfranchised : The Duel"
date: 2024-12-17
categories: ["Data story", "Milestone 3"]
---

### Univariate analysis : LOOK AT OUTLIERS AND SINGLE THEM OUT
Add to intro : After performing a Z-score test we hae 20 outiliers statisticly. 
Throught the entire analysis we will have a red line exemple, how about one of the greastest movie franchise... **FF**

How do should we compare franchise and non-franchise movies? Let's break it down step by step:

Which countries produce movies? Is there a distinction between the countries of origin for franchise and non-franchise films?

To begin, let's examine a network graph to visualize where the movies were produced and how the countries are interconnected.

{% include graphs/plot_9.html %}
{% include graphs/plot_7.html %}


To be more rigourus, let's dive in the countries repartitions: 

{% include graphs/plot_7_2}

We see that the movies coming from the United-States, Japan, Hong-Kong and Canada represent more of the total franchise movies than for non-franchise movies! 
The presence of the USA is not a surprise, everyone knows the influence of Holloywood and the multpile blockbuster franchise such as the Marvel, Superman, etc... 
How about Japan? If you go deeper, most of the franchise from Japan are reinterpreted mangas such as: Tora-san (48 movies), Doremon (33 movies) and also the well known One piece, Dragon ball Z...

Funny, **FF** is produced in 

Now, what about the **genres** of movies?

{% include graphs/plot_4.html %}
Here, we can see that Dramas and Romances are a lot more present (three and two times more, respectively) in non-franchise movies than in franchise movies. Why is that ? Do the viewers lose interest when they are presented multiple dramas in a row ? If so, how would that translate ? In worse ratings ? Less box-office revenues ? 

The opposite is true for Action, Adventure, and Science-Fiction movies : they are around twice as present in franchise movies !
Same as **FF**

What about the **actors** in movies? 
It seems that actor gender distribution remains the same for franchise and non-franchise movies. (This is unsurprising as most of us can agree that there are particulalry many female characters in franchise movies than non-franchise movies, at least anecdotally.)
{% include graphs/plot_11.html %}

What about their **ethnicity**? 
There is no relevent difference between franchise movie and non-franchise ones, only for the Asian actors. The production location does not seems to influence, therefore it could be explained by an unknown confounding feature. 
{% include graphs/plot_12.html %}


The release date distributions are relatively similar overall. However, most franchises tend to have closely spaced release periods for their entire movies. This pattern aligns with the fact that the majority of franchises consist of four movies or fewer. That said, exceptions do exist—for exemple the Bambi collection includes only two movies, but the releases are far apart (1942 and 2006).

How were they appreciated by the public ?

This is the distribution of the average score vote for both franchise and non-franchise, it is skewed distribution. The median of both are close (6.1 for franchise, 6 for non franchise), there is no important difference between the two types of movies. 

It is often said that the second movie is not as good, but is that true? What are the average score threw the different movies in a franchise? 

{% include graphs/plot_vote_general_vote_distribution.html %}

At this stage of the data analysis, the stereotype holds: the average rating tends to drop for the second movie. However, as mentioned earlier, franchise films include several outliers. So, what could be the recipe to make the best possible sequel?
{% include graphs/plot_vote_general_vote_distribution_per_movie order.html %}


How much money did they cost ?

{% include graphs/plot_13.html %}

Does franchise movie have a largest budget? Yes! 

In general it is all most the double! 

Too be as rigorous as possible all the values regarding expenses were adjusted to the inflation rate at the release time of each movies. Now we can see the “real revenue” and “real budget”.

In general franchise movies has a larger budget then the other movies, but the difference is even more significant when looking at average revenue. 

Let’s finally, ask the question on everyone’s minds: How well do they perform? How high is their box office revenue? 

{% include graphs/plot_8.html %}

Here the difference is even more flagrant! In average a franchise movie makes 5 times more box office revenue then other movies! 

Are you persuaded now that a movie in a franchise is more successful? 

What is your favorite franchise? Harry Potter, Star Wars or James Bond? 

With this interactive graph now you can see which movies in its franchise had the best box office or the lowest, and even its budget. 

SUPER INTERACTIVE PLOT 

 A franchise movie is more successful but  how can this be explained ? **What** makes them more successful ? **Why** does franchise exists ? 

What if creating a second movie was a less risky investment then one single movie. In fact, if people liked the story plot of a movie it might be likely that they’ll go see the second movie? In that case, what are the ratio between the revenue and the budget?
{% include graphs/plot_ratio_boxplot.html %}


From this boxplot we can know that the average ratio of revenue over budget is twice larger then in non-franchise movies. How ever we don't see a large evolution for sequels in franchise. 






![Dummy Image 2](https://picsum.photos/1200/400)


