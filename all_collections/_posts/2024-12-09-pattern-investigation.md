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
_Number of franchises: 28_  
_Highlight: Alvin and the Chipmunks, Dirty Dancing, High School Musical, Grease_  
It's mainly composed of musical franchise, the combination of the `music` and `drama`, looking at the franchise also helps. It is also a minority in the dataset.

**Cluster 2:**
_Number of franchises: 218_  
_Highlight: Home Alone, Toy Story, Twilight, Lion King, Happy Feet, Ice Age_  
This is one of the first really big cluster, it looks like its mostly teenage movies, animated movies, Disneys and family sitcom. The main genre is `comedy`, `family` and `adventure`.

**Cluster 3:**
_Number of franchises: 168_  
_Highlight: Star Wars, Spider-Man, Jurassic Park, Tomb Raider, The Matrix_  
Also a big cluster, it is mainly composed of `action` movies that requires a higher budget to be produced and

**Cluster 4:**
_Number of franchises: 166_  
_Highlight: Scream, Alien, The Exorcist, Resident Evil, Saw, The Human Centipede_  
Here the main genre is `horror` and `thriller`; this combination makes it really clear what type of movie this is about. A noticeable feature of those franchise is their remarkably low average budgets, this help maximizing their potential to achieve an outstanding revenue-to-budget ratio.

---

{% include graphs/franchise_clusters_2.html %}

**Outliers:** The outliers are the franchise that the algorithm couldn't group with the other franchise, we have James Bond who was already used as an example and two less known franchise that got separated for their high vote (note that those have genre closest to the horror/thriller cluster 4 that's why its consider high).

There are a few other interesting things to notice, first most of the franchise kind of perform the same in terms of ratio across every genre and budget. The thing that differentiate a franchise that performs well from one that performs really well is an outlier behavior that with this dataset cannot be explained clearly. 

However, something is still missing, we see that the general behavior of franchise successfulness varies a lot, but we have no info yet on the success inside a franchise between the different movies in a franchise. That's why in the next part we're going to look deeper at the interaction between the first and second movie trying to answer: 
> When a movie is successful, wanting to continue the story is always tempting; but how do we make a second successful movie, or even eventually, a successful franchise?


A similar clustering method was used but now to group the common feature of both the first and second movies. In order to make it more interpretable and have better insight of common behaviour the dataset was separated in two main categories:
- The franchises were the first movie has a better ratio than the second one, they were assigned a positive cluster number. (Total of 31)
- The franchises were the second movie has a better ratio, they were assigned a strictly negative cluster number. (Total of 202)

Looking at the results, we first notice that there's still common behaviour that the budget and revenue are correlated, we also observe that we have different range of budgets/revenue separated. The genre feature still has a strong impact on the clusterisation too. Another interesting fact is about the ratio. Since we grouped the franchise, a common behaviour for franchise with an increase ratio is that a decrease of the budget was done and the other way around too.

---

<div style="display: grid; grid-template-columns: 1fr 1fr; gap: 20px;">
  <div>
    {% include graphs/1_2_clusters.html %}
  </div>
  <div>
<p>
<b>Cluster -4:</b><i> Number of franchises: 8<br>
Highlight: Harry Potter, The Lord of the Rings, The Dark Knight, Ghost Rider</i>
First cluster, where the ratio has improved, it is mainly high budget movies that didn't got a significant increase of the budget for the second movie but performed even better, the vote average didn't change. It has a main genre of Action and Adventure.
</p><p>
<b>Cluster -3:</b><i> Number of franchises: 13<br>
Highlight: Ice Age, Twilight, Austin Powers </i>
This is a really interesting cluster; it looks like a part of those second movies were not really appreciated even tho it got a increased in revenue from the first movie, maybe the fame of the first movie was used to create a lowered budget one to make a second movie? Note that its mainly comedy, drama and romance, which can also sometime be genres that are harder to make a second story.
</p><p>
<b>Cluster -2:</b><i> Number of franchises: 4<br>
Highlight: Arthur and the Invisibles, World of Watches, The Transporter, The Boondock Saints</i>
This one is even more interesting, because half of the 1st movies actually lost money and they still did a second movie that go better result moneywise but not in the ratings too. Note that its a really small cluster. 
</p><p>
<b>Cluster -1:</b><i> Number of franchises: 6<br>
Highlight: Star Trek: The Original Series, Star Trek: The Next Generation, Airport</i>
This is a similar cluster to the cluster -3 but with a lower budget and revenue.
</p>
</div>
</div>

<div style="display: grid; grid-template-columns: 1fr 1fr; gap: 20px;">
  <div><p>
<b>Cluster 1:</b><i> Number of franchises: 11<br>
Highlight: James Bond Collection, Bridget Jones, Taken, Mr. Bean </i><br>
First cluster where the second movie ratio is worse, its not a big cluster. It also looks like it got a pretty clear vote difference. It's mostly recent movies and a quartile of those franchise actually have a revenue that is lower than the budget. This cluster also has maily recent movies (2000s) and medium budget.
</p>
  <p>
   <b>Cluster 2:</b><i> Number of franchises: 66<br>
Highlight: Predator, Saw, Friday the 13th, X Files, Resident Evil, Piranha 3D </i><br>
This is the horror and thriller cluster, it is also lower budget movies and we notice also that around a fourth of the 2nd movie actually don't have a higher revenue than budget.
    </p><p>
    <b>Cluster 3:</b><i> Number of franchises: 84<br>
Highlight: American Pie, Ghostbusters, Scary Movie, Legally Blonde,  Scooby-Doo, Power Rangers </i><br>
It's the comedy and family clusters, still around a fourth of the second don't have a higher revenue than a budget but its less worse.
 </p><p>
<b>Cluster 4:</b><i> Number of franchises: 41<br>
Highlight: Star Wars, Indiana Jones, Fast and the Furious, Transformers, Sherlock Holmes, The Expendables, Iron Man
</i>
This cluster and the next one are the high budget ones, that get worse result than the first movie in terms of ratio but actually it stays mostly higher than on. It means that even though the ratio is worse around the revenue stays the same, because budget increased. Here we have the action and blockbusters.
 </p>

  </div>
  <div>
     {% include graphs/1_2_clusters_2.html %}
     <p>
<b>Cluster 5:</b><i> Number of franchises: 17<br>
Highlight: Shrek, Toy Story, Happy Feet, The Jungle Book, Stuart Little, Garfield
</i>
Here we have more the comedy, animation and family movies but the behaviour is around the same.
 </p>
</div>
</div>

   {% include graphs/1_2_clusters_genre.html %}

---

To kind of answer our big question, we can summarize the observation with this: most of the second movies are actually performing less good than the first movie, however, the behavior seem to depend mostly on: what genre is the franchise, was there a budget update and what range of budget are we talking about.

Finally, this analysis is a tiny step towards a clearer explanation of the complexity of behaviors a franchise can have, which have still lost of untold secrets.
   
