---
layout: post
title: "Shapley value analysis: what is the recipe for franchise movies?"
date: 2024-12-17
categories: ["Data story", "Milestone 3"]
---
In our univarariate and bivariate analysis, we explored the wealth of information associated with each movie and the interaction between variables. However, it is difficult to conclude what variables characterize franchise movies the most from these previous analyses only.

## Shapley value comes into rescue

Instead of directly inspecting relationship between variables, we can also train a model to predict whether the subsequent movie exists for an individual movie or not, and run feature importance analysis. We use a concept from cooperative game theory called ***“Shapley value”***. The advantage Shapley value over regular feature importance is that, it also provides information about whether each feature contributes positively or negatively to the prediction! We trained `HistGradientBoostingClassifier`, a tree based model from scikit-learn and calculate Shapley values for various binary-encoded features about genres, ethnicity, country and other numerical variables.

We balanced the number of franchise and non-franchise movies in the training data by subsampling, and the model achieved **81.7% test accuracy** which is significantly better than the baseline (50% for binary prediction)! Below, we show the summary plot for Shapley value analyis:

<div style="text-align: center;">
    <img src="{{ site.baseurl }}/assets/images/shap_summary_plot.jpg" alt="SHAP Summary Plot" width="550" height="700">
</div>

Here, we're showing **the top 20 features** that have the highest mean absolute Shapley value. Recall that, these features are those of first movies in franchise or of non-franchise movies from which we constructed the dataset for this analysis. The color bar shows the distribution of values within each feature, while gray dots signify missing values. The high Shapley value (x-axis) indicates positive contribution to model's prediction (= prediction being 1, there will be a second movie), and the low Shapley value means negative contribution.

From the plot, we observe that `vote_count` has the most positive contribution when its value is high. However, this feature was drown from TMDB dataset and it is possible that franchise movies gained a lot of votes because the seris was already famous. `vote_average`(= rating by users) was also drived from TMDB, and here we see a pattern that higher rating contributes positively to the prediction. **It makes sense that the first movie in franchise has more popularity than an average movie, as that movitvates producers to create a subsequent film.** Recall that from our bivariate analysis, `vote_average` has positive linear correlation with `real_revenue` (inflation adjusted revenue). In fact, `real_revenue` does show up highly in the summary plot above, which adds coherence to our interpretation.

As for movie genres, we see that **Family, Action, Comedy and Fantasy films are more likely to be franchised**. This partially supports our earlier analysis, highlighting that Action, Adventure, and Science Fiction genres are twice as common in franchises. In contrast, Fantasy and Animation films are less frequent in franchise movies (from univariate analysis), however, bivariate analysis of genres and revenue revealed that these two genres (which are often present together with Family genre) were among the three most profitable genres. Again, since `real_revenue` shows up as the 4th most important feature, this is logical. The low contribution of `is_drama` validates the previous analysis, where this genre was more frequent in non-franchise movies.

While contribution from racial group is rather minor, we see some contribution from `from_US` (whether the movie was produced in the US or not). We expected that this feature would positively contribute to the prediction as the majority of franchise movies comes from the US in our dataset whereas this is not the case for non-franchise movies. However, the plot shows the negative contribution of this feature. Perhaps, `from_US` is highly dependent on another feature such as genres which makes its interpretation difficult.