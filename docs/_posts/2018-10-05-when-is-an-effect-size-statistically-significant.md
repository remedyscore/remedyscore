---
layout: post
title: When Is An Effect Size Statistically Significant?   
description: An overview of measures to estimate statistical significance, including p-values, alpha, and confidence intervals
tags: Effect_Sizes Confidence_Intervals
---

{% include image.html name="header_17_resized.jpg" alt="When Is An Effect Size Statistically Significant" class="header-image" %} 

<p style="color: grey"><i>An overview of measures to estimate statistical significance, including p-values, alpha, and confidence intervals</i></p>


<!--more-->

## Overview

When attempting to determine if an Effect Size is statistically significant, we first create a **Null Hypothesis ("H0")** that a given treatment failed to demonstrate a measurable effect.  We then test an Alternative Hypothesis that states a given treatment succeeded in demonstrating a measurable effect, and therefore rejects our initial Null Hypothesis.

In testing our **Alternative Hypothesis** (and therein rejecting our Null Hypothesis), we must commit to two key values: 

* **Alpha:**  The significance level (alpha level) that a test result must show for the Alternative Hypothesis to prove more compelling than the Null Hypothesis.  This is typically set at 1%, 5%, or 10% - and implies we may only reject the Null Hypothesis if the observed data are so unusual that they would have only occurred by chance at most 1%, 5%, or 10% of the time.  Note that we often frame Alpha in terms of a desired **Confidence Interval** - which is simply calculated as Confidence Interval = 1 - Alpha.  So, for example, if Alpha equals 5% than the Confidence Interval equals 95% (less than 1 in 20 chance that we incorrectly claim statistical significance).

* **Type I Error:**  The amount of risk we will accept that our Alternative Hypothesis incorrectly proved more compelling than the Null Hypothesis

We then perform the experiment and after it concludes we compare our desired significance level (Alpha) to experiment's *P-Value* or Probability Value that our results are due to chance.

* **P-Value <= Alpha:**  We reject the null hypothesis, find our treatment and control groups to be different, and say our results are statistically significant 

* **P-Value > Alpha:**  We fail to reject the null hypothesis, find there is at least a [5%] probability our treatment and controls groups are the same, and say the results are statistically nonsignificant.

So, for example, if our Confidence Interval is 95% - and therefore our Alpha value is 5% - and we run our experiment and get a P-Value of 3%, we can say our results are statistically significant (3% P-Value <= 5% Alpha value).  Put differently, there is only a 3% chance that our treatment and control groups are the same, and therefore we have 97% confidence the groups are different; this exceeds our desire to have 95% confidence in our decision to move forward – and therefore, we claim statistical significance.  Conversely, if our P-Value was 6%, this would exceed our comfort-level for a less than 5% probability the groups are similar, and mean our results are not statistically significant at a 95% Confidence Interval. 

Visually, low P-Values imply our results are in the corners or "tails" of the normal distribution curve (i.e.; they are extreme and it would be quite unusual for them to be false).  However, because we typically don't know if the results will fall into the left or right corner/tail - it is standard practice to perform a **Two-Tailed Test**.  This means the calculated P-Value is multiplied by two to account for both tails of the normal distribution curve, and then compared to Alpha.  The Two-Tailed Test gives more confidence in a given experiment by simultaneously making it (a) harder to achieve statistical significance and (b) decreasing the risk of Type I Error.

This being said, it is sometimes possible to **P-Hack** by selectively removing data from a dataset, until the P-Value falls below a target Alpha value.  This is viewed as performing biased and illegitimate research. 


## More About Confidence Intervals

As established, there is a close relationship between Confidence Intervals and statistical significance.  Confidence Intervals are the range of values that contain a calculated Effect Size with a degree of probabilistic certainty (typically a 95% certainty or confidence-level).   So, for example, a Standardized Mean Difference might be estimated at 0.22 - but we believe with high certainty (95% certainty) it falls between 0.04 (Starting Confidence Interval) to 0.40 (Ending Confidence Interval).

There are, however, some values that when included in a Confidence Interval immediately negate any statistical significance of the calculated effect size: 

<table>
    <thead>
        <tr>
            <th style="text-align: left;">Effect Size</th>
            <th style="text-align: center;">Confidence Interval Shouldn't Contain</th>
            <th style="text-align: left;">Because</th>
            <th style="text-align: left;">For Example</th> 
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="text-align: left;"><p>
                <b>Continuous</b>
                (Standardized Mean Difference)            
            </p></td>
            <td style="text-align: center;">0</td>
            <td style="text-align: left;">When the Standardized Mean Difference equals zero it means there is no difference between the treatment and control group</td>                
            <td style="text-align: left;">If the Continuous Confidence Interval equaled 0, it means there is no difference between the treatment and control group - which means a difference has not be definitively established, and our result may not be statistically significant.</td>            
        </tr>
        <tr>
            <td style="text-align: left;"><p>
                <b>Dichotomous</b>
                (Odds Ratio)            
            </p></td>
            <td style="text-align: center;">1</td>
            <td style="text-align: left;">When Odds / Risk Ratio equals one it means there is no difference between the treatment and control group</td>
            <td style="text-align: left;">If the Dichotomous Confidence Interval equaled 1, it means the true value might be 1 and therefore the groups have no difference. </td>
        </tr> 
    </tbody>
</table>    

In summary, when we are calculating an Effect Size between two different groups, we are hoping there is a statistically significant difference between the groups.  In this case, 'significant' is shorthand for 'significantly different from zero/one' – because when zero or one is included in a Confidence Interval it means the results could be the same (not different).

For example: 

* CI Start (-0.08) and CI End (1.81) would be deemed statistically insignificant for an Odds Ratio or Standardized Mean Difference (P-Value > Alpha)
* CI Start (0.06) and CI End (1.52) would be deemed statistically significant for Standardized Mean Difference, but not an Odds Ratio (P-Value < Alpha)

So, checking starting and ending confidence intervals can also help determine statistical significance. 
