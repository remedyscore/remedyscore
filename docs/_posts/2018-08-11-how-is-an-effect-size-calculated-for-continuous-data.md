---
layout: post
title: How Is An Effect Size Calculated For Continuous Data?   
description: An overview of calculating and interpreting an effect size for continuous data including Cohen's d and Hedge's g 
tags: Effect_Sizes Continuous_Data  
---

{% include image.html name="header_12_resized.jpg" alt="How Is An Effect Size Calculated For Continuous Data" class="header-image" %} 

<p style="color: grey"><i>An overview of calculating and interpreting an effect size for dichotomous data including Cohen's d and Hedge's g</i></p>


<!--more-->

When a study contains Continuous Data (numeric data along a range, such as weight, blood pressure, etc.), a standardized mean difference is typically calculated as the effect size.  The formula to calculate a standardized mean difference is as follows:
 
(Mean of Treatment Group Outcome – Mean of Control Group Outcome) / Pooled Standard Deviation

In words, this means we take the difference in mean outcomes between the treatment and control group and normalize it using the standard deviation based on both populations.  Multiple methods exist to calculate a pooled standard deviation:
  
* **Cohen's d:**  The most basic means of calculating a pooled standard deviation is using a formula called Cohen's d.  However, when Cohen's d is used to calculate Effect Size, the result tends to be overstated in smaller populations (below twenty).  This can lead researchers to overemphasize the favorability of a particular intervention, despite it actually having a fairly weak effect.  See below [the formula](https://www.meta-analysis.com/downloads/Meta-analysis%20Effect%20sizes%20based%20on%20means.pdf) for calculating Pooled Standard Deviation when deriving Cohen's d:

  {% include image.html name="cohen_pooled_standard_dev.png" alt="cohen pooled standard deviation" class="header-image" %} 
 
* **Hedge's g:**  To correct for the deficiencies in Cohen's d, the pooled standard deviation can be [calculated](http://www.stat-help.com/Meta%20analysis%202009-07-31.pdf) using Hedge's g, which includes a correction factor (Bessel's correction) for smaller sample sizes.  Specifically, Bessel's correction involves subtracting one from each sample observation ("n") in the formula for Pooled Standard Deviation.  So, in the case of Hedge's g, the Pooled Standard Deviation is calculated by subtracting two from the denominator, because we have two sample observations (treatment and control):

  {% include image.html name="hedge_pooled_standard_dev.png" alt="hedge pooled standard deviation" class="header-image" %} 
 
* **Hedge's g\* / Hedge's d:**  We can go one step further, and refine Hedge's g even further to avoid overstating the value of the Effect Size when dealing with smaller samples.  To do so, we multiple Hedge's g by a [correction factor](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3840331/) sometimes called "[J](https://www.meta-analysis.com/downloads/Meta-analysis%20Effect%20sizes%20based%20on%20means.pdf)", which is calculated as (1 – (3 / (4 * (Treatment Population + Control Population – 2) – 1) )).  This refined version of Hedge's g lacks a uniform naming convention, but is typically called Hedge's d or Hedge's g*.  That being said, some researchers have called the prior calculation (with Bessel's correction) Cohen's d and this "corrected" calculation Hedge's g.  So, the naming conventions for Pooled Standard Deviations remain somewhat ambiguous, in spite of the calculations being consistent and clear. 

Finally, it is worth reiterating that these correction factors become less relevant as an experiment's population size increases, given that they are specifically meant to avoid overstating experiments with small population sizes.  So, typically a correction factor like "J" will be fairly close to "1" unless the total sample size is fairly small (for example, less than ten) - so it should play a very small role when calculating a final Effect Size for a given study.  Put differently, Hedge's g* and Cohen's d are almost identical, until the sample population begins approaching ten.

That said, once an Effect Size based on the Standardized Mean Difference has been derived, it can be interpreted as follows:

<table>
    <thead>
        <tr>
            <th style="text-align: left;">
                <p>Continuous Data</p> 
                <p>(Standard Mean Difference)</p>
            </th>
            <th style="text-align: left;">Interpretation</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="text-align: left;">
                <p><b>Standard Mean Diff > 0</b></p>
                <p><b>(Treatment > Control)</b></p>
            </td>
            <td style="text-align: left;">Mean outcome is increased in the treatment group when compared to the control group</td>
        </tr>  
        <tr>
            <td style="text-align: left;">
                <p><b>Standard Mean Diff = 0</b></p>
                <p><b>(Treatment = Control)</b></p>
            </td>
            <td style="text-align: left;">No difference between the treatment and control</td>
        </tr>  
        <tr>
            <td style="text-align: left;">
                <p><b>Standard Mean Diff < 0</b></p>
                <p><b>(Treatment < Control)</b></p>
            </td>
            <td style="text-align: left;">Mean outcome is decreased in the treatment group when compared to the control group</td>
        </tr>                                     
    </tbody>
</table>
