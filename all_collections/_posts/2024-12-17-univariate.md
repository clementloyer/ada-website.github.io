---
layout: post
title: "Franchised vs. Unfranchised : The Duel"
date: 2024-12-17
categories: ["Data story", "Milestone 3"]
---

## Univariate analysis : 
In this section, we'll look at each feature of our movies (stay tuned !) and compare them with non-franchised movies in order to look for eventual differences. As a bonus, throughtout the entire data story, we will highlight a franchise to illustrate our discoveries. How about one of the greastest movie franchise of all times ? ... **Star Wars**

But let's get back to business : which features should we look at ?

### Genres
First, what about the **genres** of movies?

{% include graphs/plot_4.html %}
Here, we can see that Dramas and Romances are a lot more present (three and two times more, respectively) in non-franchise movies than in franchise movies. The opposite is true for Action, Adventure, and Science-Fiction movies : they are around twice as present in franchise movies! Why is that ? Do the viewers lose interest when they are presented multiple dramas in a row ? If so, how would that translate ? In worse ratings ? Less box-office revenues ? We'll see ...

What a coincidence ! **Star Wars** has exaclty those genres!

### Time representation
The release date distributions are relatively similar overall. However, most franchises tend to have closely spaced release periods for their entire movies. This pattern aligns with the fact that the majority of franchises consist of four movies or fewer. That said, exceptions do exist —for exemple the Bambi collection includes only two movies, but the releases are far apart (1942 and 2006).

{% include graphs/Franchise_density.html %}
### Countries repartition
How about we ask ourselves which countries produce movies? Do some countries produce (and therefore consume) more franchise movies ?

To begin, let's examine a network graph to visualize where the movies were produced and how the countries are interconnected.
Franchise movies : 
{% include graphs/plot_9.html %}

Other movies : 

{% include graphs/plot_7.html %}

Humm, as pretty as it is, nothing meaningful can be extracted from these maps ... Let's look closer :

{% include graphs/plot_7_3.html %}
We see that the movies coming from the United-States, Japan, Hong-Kong and Canada represent more of the total franchise movies than for non-franchise movies! 
The presence of the USA is not a surprise, everyone knows the influence of Holloywood and the multpile blockbuster franchise such as the Marvel, Superman, etc... 

How about Japan? If you go deeper, most of the franchise from Japan are reinterpreted mangas such as: Tora-san (48 movies), Doremon (33 movies) and also the well known One piece, Dragon ball Z...

Funny, **Star Wars** is produced in the United-State!
### Is there a difference in public appreciation between franchise movies and non-franchise movies?

To first get a sense at franchise movies are received by the publice in general, let's look at the distribution below : for now, when comparing franchises as a whole, the difference in franchise vs non-franchised movies isn't striking. **Star Wars** has a rate of 7,5, it is not surp^ising that this famous saga is above the average. But it doesn't stop here !

 
{% include graphs/plot_17.html %}
 

### Actor identity analysis

Racial bias is an important topic in the movie industry and we were interested in **whether the actors of certain ethnicity/gender groups appear more or less commonly in franchise movies**. Are they depicted positively (*hero/heroine*) or negatively (*villain*)?

To begin with, we look at actor gender distribution of franchise and non-franchise movies.

{% include graphs/plot_11.html %}

It seems that actor gender distribution remains the same for franchise and non-franchise movies. **This is unsurprising as we can agree that there are particulalry many female characters in franchise movies than non-franchise movies**, at least anecdotally.

Next, we shift our focus to ethnicity groups. Contrary to actor gender information, actor ethnicity is not available for the majority of actors (available for 99719/395202 = 25.2%)... Upon observing the dataset, **we hypothesized that the actors with known ethnicity are those with more publicity**, so they are more likely to play main roles in the movies. The ethnicity distribution of these main actors can be representative of which racial group is more or less featured in the movie. Having this in mind, we will proceed to visualize actors' racial group distribution for franchise and non-franchise movies.
{% include graphs/plot_12.html %}


The percentages in each of the plots above sum up to 100%. Notice that **compared to non-franchise movies, franchise movies have fewer percentage of Asian actors** (Franchise: 14.78%, Non-franchise: 31.18%). If we compared this to the 4 pie charts from the previous section above, the two pie charts on the righthand side of the figure show that the proporitions of movies from Asia (excluding Russia, Oceania and Middle East) in franchise and non-franchise movies are not as different as the disparity observed earlie in Asian actor percentages.

This means that **the disparity in the percentage of Asian actors comes from factors other than movie production location**. It is hard to identify the exact cause for this from our analysis only, but a potential confounding factor is the difference in genres: perhaps certain movie genres are more likely to be franchised which are underrepresented by Asian actors.

#### Sentimental analysis
In this section, we examine the narrative of each character in movie plots. We leveraged GPT o4-mini to extract adjectives related to each character, and calculate sentiment scores using TextBlob by taking an average of sentiment scores for adjectives. We show examples of positive and negative adjectives extracted:

<div style="text-align: center;">
    <img src="{{ site.baseurl }}/assets/images/plot_30.jpg" alt="SHAP Summary Plot" width="550" height="700">
</div>

We also plot the distribution of sentiment score per racial group. Note that among 99719 actors whose ethnicity information is available, we could only extract adjectives for 31095 characters (=actors). This is because some characters are not mentioned in the movie plot at all.

{% include graphs/plot_14.html %}

It seems like there is not much difference in the inter-quantile ranges (Q3-Q1) across groups. With our dataset, we did not have enough actors with ethnicity information to conduct the sentiment analysis per genre per country, but if we were able to do that, this could have illustrated the racial bias existant in the movie industry such as which group is more likely to play a hero/heroin role in romance movies.

### Movie revenue box office and their budget 
And finally, the **money question** ! First, how much did these movies cost to produce ?

So, do franchise movies have a larger budget? Overall, yes! Almost twice as much ! 

To be as rigorous as possible, all the values regarding expenses were adjusted to the inflation rate at the release time of each movie. Now we can see the “real revenue” and “real budget”.

{% include graphs/plot_13.html %}

And now, the question on everyone’s minds: How well do they perform? **How much money do they bring back ?** 
{% include graphs/plot_8.html %}

Here the difference is even more flagrant! In average a franchise movie makes 5 times more box office revenue then other movies! 

Are you persuaded now that a movie in a franchise is more successful? 

What is your favorite franchise? Harry Potter, Star Wars or James Bond? 

With this interactive graph now you can see which movies in its franchise had the best box office or the lowest, and even its budget. 

<iframe 
        src="https://lavine.pythonanywhere.com/"
        style="width: 100%; height: 950px; border: none; border-width: 1px;"> 
        
</iframe>



 A franchise movie is more successful but  how can this be explained ? **What** makes them more successful ? **Why** does franchise exists ? 

What if creating a second movie was a less risky investment then one single movie. In fact, if people liked the story plot of a movie, it's probably likely that they’ll go see the second movie right? In that case, what is the ratio between the revenue and the budget of our movies? Go to the next page to elaborate this new idea.



![Dummy Image 2](https://picsum.photos/1200/400)


