---
layout: post
title: How Many Studies Are Required To Conduct A Meta-Analysis?  
description: An overview of the number of studies recommended for a meta-analysis and means to mitigate risks inherent in meta-analyses with low study counts 
tags:  Medical_Studies Meta_Analysis Effect_Sizes 
---

{% include image.html name="header_6_resized.jpg" alt="How Many Studies Are Required To Conduct A Meta-Analysis" class="header-image" %} 

<p style="color: grey"><i>An overview of the number of studies recommended for a meta-analysis and means to mitigate risks inherent in meta-analyses with low study counts</i></p>


<!--more-->

A meta-analysis can technically be conducted with only two studies.  However, when we have only a small number of studies (two to four studies, for example), it may be impossible to estimate the variance between studies ('tau-squared' or 'τ2'), which is utilized in a Random Effects Model to combine together multiple Effect Sizes.  Put differently, when trying to guess a tau-squared distribution with only two or three studies, our guess of that distribution is unlikely to be very precise.  

So, in the event only a small number of studies exist, [options](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2667312/) include:

* Utilize a Fixed Effects Model (although this may understate differences between studies);

* Substitute tau-squared from other, similar meta-analyses; or 

* Simply consider individual studies in isolation

To help flag meta-analyses with less than three studies, RemedyScore provides users with a message that states, "Degrees of freedom for this analysis do not exceed three; results may materially change as more data is added.  To help offset some portion of this issue, consider referencing the fixed effect size."

