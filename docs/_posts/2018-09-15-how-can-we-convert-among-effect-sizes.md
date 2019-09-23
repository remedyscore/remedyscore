---
layout: post
title: How Can We Convert Among Effect Sizes?   
description: An overview of converting between dichotomous and continuous effect sizes 
tags: Effect_Sizes Dichotomous_Data Continuous_Data 
---

{% include image.html name="header_15_resized.jpg" alt="How Can We Convert Among Effect Sizes" class="header-image" %} 

<p style="color: grey"><i>An overview of converting between dichotomous and continuous effect sizes</i></p>


<!--more-->

## Overview

To simplify interpretation of Effect Sizes – which might be calculated as an Odds Ratio (Dichotomous Data) or Standardized Mean Difference (Continuous Data) – it can be helpful to [convert](https://www.meta-analysis.com/downloads/Meta-analysis%20Converting%20among%20effect%20sizes.pdf) [between](https://www.um.es/metaanalysis/pdf/7078.pdf) them.  This allows a [common metric](https://campbellcollaboration.org/media/k2/attachments/converting_between_effect_sizes.pdf) to be used when synthesizing and comparing Effect Sizes.

[Multiple methods](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.468.3058&rep=rep1&type=pdf) have been developed to convert between Odds Ratios and Standardized Mean Differences; each of which has specific advantages and disadvantages.  For example, when converting a specific Odds Ratio - the resultant Standardized Mean Difference might range between 0.406 - 0.524 when attempting to approximate an actual value of 0.500.
 
That being said, two particular methods of conversion are most commonly utilized:
 
## Cox:

Initially developed in the 1980s, [Cox](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.468.3058&rep=rep1&type=pdf) took a [simple approach](https://robertgrantstats.wordpress.com/2012/10/19/converting-continuous-to-binary-outcomes-for-meta-analysis/) and applied the standard deviation of a normal distribution (1.65) to the Log(Odds Ratio), assuming variances are equal between groups.

* **Dichotomous To Continuous:**  
  
  * **Standardized Mean Difference:**  Log Odds Ratio / 1.65
  
  * **Continuous Variance:**  (Standard Error^2) * 0.367
   
* **Continuous To Dichotomous:**  
  
  * **Odds Ratio:**  EXP(Standardized Mean Difference * 1.65)
  
  * **Dichotomous Variance:**  Continuous Variance / 0.367
  
## Hasselblad and Hedges:

Developed a decade after Cox, [Hasselblad and Hedges](https://www.meta-analysis.com/downloads/Meta-analysis%20Converting%20among%20effect%20sizes.pdf) instead applied the standard deviation of a logistic distribution (1.81 or SQRT(3)/PI()) to the Log(Odds Ratio), also assuming variances are equal between groups.

* **Dichotomous To Continuous:**  

  * **Standardized Mean Difference:**  Log(Odds Ratio) * ( SQRT(3) / PI() ) 

  * **Continuous Variance:**  (Standard Error^2) * (3 / PI()^2) 

* **Continuous To Dichotomous:**  

  * **Odds Ratio:**  EXP(Standardized Mean Difference * ( PI() / SQRT(3) ))

  * **Dichotomous Variance:**  Continuous Variance * ( PI()^2 / 3 )

## Conclusion

The question then might follow, which method is most accurate? 

* In [one study](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.468.3058&rep=rep1&type=pdf), when seven possible means of converting values were applied to 10,000 studies via a Monte Carlo simulation, Hasselblad & Hedges ranked 4th (in the middle) for accuracy, and Cox ranked first.
 
* In [another study](https://academic.oup.com/ije/article/41/5/1445/711693), Hasselblad & Hedges surpassed Cox; predicting a 0.97 (0.91–1.04) value for a collection of odds ratios - compared to Cox's 0.92 (0.86–0.99) - when the actual value was 1.00.

* [Another study](https://academic.oup.com/ije/article/41/5/1445/711693) (Anzures-Cabrera) also pointed towards Hasselblad & Hedges as an "approximation being closest to the observed estimate"

In the end, selection of the correct conversion factor depends upon the underlying data:

* **Data Follows Normal Distribution:**  Cox methodology is more accurate

* **Data Follows Logistic Distribution:**  Hasselblad & Hedges methodology is more accurate

In either case, however, none of the conversion methodologies are entirely accurate - and you will lose some level of precision when converting between Dichotomous Data (via an Odds Ratio) and Continuous Data (via a Standardized Mean Difference).  However, the alternative - of not converting the data at all - implies a large loss of information, and is usually less preferable. At present, RemedyScore converts Effect Sizes calculated using an Odds Ratio into a Standardized Mean Difference, as Continuous Data seems a bit more common than Dichotomous Data.

It should also be noted that any Odds Ratios converted using the above formulas will result in a Standardized Mean Difference calculated with Cohen's d – and will need to be multiplied by a correction factor ("J") to account for studies with low sample sizes, and derive a Standardized Mean Difference associated with Hedge's g.

