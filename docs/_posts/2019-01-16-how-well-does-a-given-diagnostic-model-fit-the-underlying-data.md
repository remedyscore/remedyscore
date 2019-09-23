---
layout: post
title: How Well Does A Given Diagnostic Model Fit The Underlying Data?    
description: An overview of using Akaike and Bayesian Information Criteria to understand how well a diagnostic model fits the underlying study data 
tags: Diagnostic_Tests Information_Criterion
---

{% include image.html name="header_27_resized.jpg" alt="How Well Does A Given Diagnostic Model Fit The Underlying Data" class="header-image" %} 

<p style="color: grey"><i>An overview of using Akaike and Bayesian Information Criteria to understand how well a diagnostic model fits the underlying study data</i></p>


<!--more-->

While an HSROC or Bivariate Model can derive an Area Under the Curve (AUC) value, it is also beneficial to understand how well a given model may reflect (a) our underlying population and (b) extrapolate to a wider population.

Information criteria methods are used to [assess model fit](https://www.researchgate.net/post/Is_there_any_reason_to_choose_either_of_AIC_or_BIC_over_the_other) by taking a given model, and seeing how well it fits the original data set and a wider population.  Models that [score lowest](https://web.as.uky.edu/statistics/users/pbreheny/760/S13/notes/3-28.pdf) for a given information criteria are preferred, as it implies they have less variability.  There are two common means of assessing model fit: 

* **Akaike Information Criterion:**  Less intensely penalizes models with a high number of parameters

* **Bayesian Information Criterion:**  [More](https://www.researchgate.net/post/Is_there_any_reason_to_choose_either_of_AIC_or_BIC_over_the_other) [intensely](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=6&cad=rja&uact=8&ved=0ahUKEwjxhuK-6JzaAhXyTN8KHY_iCYsQFghgMAU&url=http%3A%2F%2Fpeople.musc.edu%2F~elg26%2Fteaching%2Fmethods2.2010%2Flectures%2Flect16.ppt&usg=AOvVaw0O3TLgUM7SdMkIpKm8PpLA) penalizes models with a high number of parameters 

In [most instances](https://stats.stackexchange.com/questions/577/is-there-any-reason-to-prefer-the-aic-or-bic-over-the-other) AIC and BIC will agree upon a preferred model; but BIC is particularly [helpful](https://web.as.uky.edu/statistics/users/pbreheny/760/S13/notes/3-28.pdf) when presented with a very complex model that might fit a specific data set but fail to generalize to a wider population. 
