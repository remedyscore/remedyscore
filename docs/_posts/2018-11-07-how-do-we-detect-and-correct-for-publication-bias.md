---
layout: post
title: How Do We Detect And Correct For Publication Bias?   
description: An overview of strategies to identify publication bias (funnel plots, Egger's regression) and correct for it
tags: Medical_Studies Publication_Bias
---

{% include image.html name="header_20_resized.jpg" alt="How Do We Detect And Correct For Publication Bias" class="header-image" %} 

<p style="color: grey"><i>An overview of strategies to identify publication bias (funnel plots, Egger's regression) and correct for it</i></p>


<!--more-->

Publication bias is a phenomenon that researchers and scientific journals [tend to](https://www.meta-analysis.com/downloads/Publication%20bias.pdf) publish studies that show significant positive findings.  Research that shows an intervention lacks a positive effect is less likely to be newsworthy, so it is sometimes simply filed-away by the researcher and/or journal.  Unfortunately, this data is effectively lost when systematically reviewing a particular intervention, and might cause a biased interpretation of the intervention's effectiveness. 

The most [common methods](https://www-users.york.ac.uk/~mb55/msc/systrev/week7/pub_text.pdf) for assessing publication bias is using a funnel plot and Egger's linear regression test.  Both techniques seek to identify an asymmetry in the clustering of studies; particularly looking for missing negative or null studies, which were never published because they lacked significant positive findings.  In both cases, it is important to have multiple studies and preferably one of 'medium' size before making claims about the possibility of publication bias.  

Starting with a funnel plot, all studies are often placed on a graph with effect size on the x-axis and standard error on the y-axis, with data-points (hopefully) creating a funnel-like effect.  Egger's regression test then creates a regression line and checks the probably ("p-value") that this line [intercepts the origin](https://books.google.com/books?id=Vd4VpxiJp5QC&lpg=PA101&ots=WIYo2rjPgW&dq=egger+linear+regression+intercept&pg=PA101&hl=sl#v=onepage&q=egger%20linear%20regression%20intercept&f=false) (zero value) of the given funnel plot.  The more the regression line deviates from intercepting the origin, the more asymmetry is believed to exist in the funnel plot and underlying studies composing the meta-analysis.  As a rule of thumb, when the regression line has a probability (one-tailed p-value) of [intersecting the origin](https://stats.stackexchange.com/questions/7040/egger-s-linear-regression-method-intercept-in-meta-analysis) of 10% (0.10) or less, the existence of asymmetry is considered to be statistically significant and publication bias is believed to be in play.

In the event an Egger regression detects publication bias (see calculations in Microsoft Excel [here](http://www.erim.eur.nl/research-support/meta-essentials/user-manual/work-with-the-workbooks/publication-bias-analysis-sheet/egger-regression-and-begg-and-mazumdar-rank-correlation-test/)), a [Trim and Fill Method](https://www.meta-analysis.com/downloads/Smoking.pdf) is used to remove some studies and impute the 'missing' studies.  To do this, we first eliminate the largest study on the other side of a given funnel plot - and replace it with a similarly imputed study on the other side of the funnel plot.  This process repeats until we believe all missing studies have been added and we have effectively balanced the funnel plot. 
