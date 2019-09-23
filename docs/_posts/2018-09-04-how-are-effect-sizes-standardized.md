---
layout: post
title: How Are Effect Sizes Standardized?   
description: An overview of methods for calculating effect sizes in a consistent manner 
tags: Effect_Sizes Dichotomous_Data Continuous_Data 
---

{% include image.html name="header_14_resized.jpg" alt="How Should Effect Sizes Be Interpreted" class="header-image" %} 

<p style="color: grey"><i>An overview of methods for calculating effect sizes in a consistent manner</i></p>


<!--more-->


Effect Sizes are entirely *relative* to the outcome being measured:

<table>
    <thead>
        <tr>
            <th style="text-align: left;">Dichotomous (Odds Ratio)</th>
            <th style="text-align: left;">Large Effect Size Is Good</th>
            <th style="text-align: left;">Small Effect Size Is Good</th>            
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="text-align: left;"><b>Odds / Risk Ratio</b></td>
            <td style="text-align: left;">People given a class are 2.50 times as likely to pass high school compared to people that didn't take the class</td>
            <td style="text-align: left;">People given aspirin are 0.58 times as likely to have a heart attack compared to people that didn't take aspirin </td>
        </tr>
        <tr>
            <td style="text-align: left;"><b>Hedge's G</b></td>
            <td style="text-align: left;">People given a class score 0.8 standard deviations above people that didn't take the class</td>
            <td style="text-align: left;">People doing yoga have depression levels -2.29 standard deviations below people that do not do yoga</td>
        </tr>                                 
    </tbody>
</table>

We see above that both large and small effect sizes can both be associated with a positive outcome.  The interpretation of the effect size all depends upon the outcome being measured.

That being said, the Odds Ratio and Hedge's G [do not correct](http://handbook-5-1.cochrane.org/chapter_9/9_2_3_2_the_standardized_mean_difference.htm) for the differences in direction when measuring a particular outcome.  The task of standardizing a particular set of effect sizes is the duty of the individual gathering and synthesizing the data.

To create a level of consistency when analyzing effect sizes, it is recommended to standardize them so the scales all point in the same direction:

<table>
    <thead>
        <tr>
            <th style="text-align: left;">Effect Size</th>
            <th style="text-align: center;">Treatment Succeeds</th>
            <th style="text-align: center;">Treatment Fails</th>            
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="text-align: left;"><b>Dichotomous Data</b></td>
            <td style="text-align: center;"> Odds / Risk Ratio > 1</td>
            <td style="text-align: center;"> Odds / Risk Ratio < 1 </td>
        </tr>
        <tr>
            <td style="text-align: left;"><b>Continuous Data</b></td>
            <td style="text-align: center;"> Hedge's G > 0 </td>
            <td style="text-align: center;"> Hedge's G < 0 </td>
        </tr>                                 
    </tbody>
</table>

In particular, for Dichotomous Data it is [recommended](http://pareonline.net/getvn.asp?v=11&n=7) [to](http://www.talkstats.com/showthread.php/47356-Proper-Interpretation-of-odds-ratio-less-than-1-for-my-study) [standardize](http://docwatson.faculty.asu.edu/mco463/odds.html) any reported Odds / Risk Ratios as above 1.0 when the target treatment succeeds, given that:
 
* The magnitude of whole numbers are [easier](https://www.researchgate.net/post/How_to_interpret_odds_ratios_that_are_smaller_than_1) for people to understand than decimals; 

* Ratios below 1.0 do not have a [linear relationship](http://pareonline.net/getvn.asp?v=11&n=7) making them difficult to compare; and

* This allows for an intuitive correlation that an Effect Size grows larger as a treatment is demonstrated to be more "successful" (as opposed to getting smaller)

With this context, it is fairly easy to standardize our prior Effect Sizes by inverting the measured outcome:

<table>
    <thead>
        <tr>
            <th style="text-align: left;">Data Type</th>
            <th style="text-align: left;">Scenario</th>
            <th style="text-align: left;">Treatment Succeeds</th>            
            <th style="text-align: left;">Treatment Fails</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="text-align: left;"><b>Dichotomous</b></td>
            <td style="text-align: left;"><b>Unstandardized</b></td>
            <td style="text-align: left;"> People given aspirin are <u>0.58</u> times as likely to have a heart attack compared to people that didn't take aspirin </td>
            <td style="text-align: left;"> People given aspirin are <u>2.00</u> times as likely to have a heart attack compared to people that didn't take aspirin </td>
        </tr>
        <tr>
            <td style="text-align: left;"><b>Dichotomous</b></td>
            <td style="text-align: left;"><b>Standardized</b></td>
            <td style="text-align: left;"> People <u>not</u> given aspirin are <u>1.72</u> (1 / 0.58) times as likely to have a heart attack compared to people that did take aspirin </td>
            <td style="text-align: left;"> People <u>not</u> given aspirin are <u>0.50</u> (1 / 2.00) times as likely to have a heart attack compared to people that did take aspirin </td>        
        </tr>                                 
    </tbody>
</table>

<table>
    <thead>
        <tr>
            <th style="text-align: left;">Data Type</th>
            <th style="text-align: left;">Scenario</th>
            <th style="text-align: left;">Treatment Succeeds</th>            
            <th style="text-align: left;">Treatment Fails</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="text-align: left;"><b>Continuous</b></td>
            <td style="text-align: left;"><b>Unstandardized</b></td>
            <td style="text-align: left;"> People doing yoga have depression levels <u>-2.29</u> standard deviations below people that do not do yoga </td>
            <td style="text-align: left;"> People doing yoga have depression levels <u>3.00</u> standard deviations above people that do not do yoga </td>
        </tr>
        <tr>
            <td style="text-align: left;"><b>Continuous</b></td>
            <td style="text-align: left;"><b>Standardized</b></td>
            <td style="text-align: left;"> People <u>not</u> doing yoga have depression levels <u>2.29</u> standard deviations above people that do yoga </td>
            <td style="text-align: left;"> People <u>not</u> doing yoga have depression levels <u>-3.00</u> standard deviations below people that do yoga </td>        
        </tr>                                 
    </tbody>
</table>


In summary, of the above, we can mathematically an invert an Effect Size's direct as follows: 

* **Dichotomous Data:**  Take the Odds Ratio's [inverse](https://www.researchgate.net/post/How_to_interpret_odds_ratios_that_are_smaller_than_1) (reciprocal) and also inverse the category descriptions

* **Continuous Data:**  Take [the](https://stats.stackexchange.com/questions/233556/how-to-transform-a-negative-effect-into-positive-how-to-reverse-the-effect-dire) [negative](http://handbook-5-1.cochrane.org/chapter_9/9_2_3_2_the_standardized_mean_difference.htm) (multiply by –1) of the standardized mean difference and also inverse the category descriptions (leave [standard](http://handbook-5-1.cochrane.org/chapter_9/9_2_3_2_the_standardized_mean_difference.htm) [deviation](https://stats.stackexchange.com/questions/233556/how-to-transform-a-negative-effect-into-positive-how-to-reverse-the-effect-dire) unchanged)

In both cases, it is also possible to crudely approximate the above changes by switching any inputted treatment and control data (but the source data will no longer make sense to a third party).

The result, in either instance, is the following standardized way of reporting effect sizes:

<table>
    <thead>
        <tr>
            <th style="text-align: left;">Treatment Succeeds By...</th>
            <th style="text-align: left;">Endpoint Examples</th>
            <th style="text-align: left;">Effect Size Reporting</th>            
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="text-align: left;"><b>Diminishing Negative Endpoint</b></td>
            <td style="text-align: left;"> 
                <ul>
                    <li>Heart Attacks</li>
                    <li>Tumors</li>
                    <li>Mortality (Death)</li>                    
                </ul>            
            </td>
            <td style="text-align: left;"> People NOT given treatment are [X.XX] times as likely to have negative endpoint compared to people not given treatment  </td>
        </tr>
        <tr>
            <td style="text-align: left;"><b>Increasing Positive Endpoint</b></td>
            <td style="text-align: left;">
                <ul>
                    <li>Mobility</li>
                    <li>Quality of Life</li>
                    <li>Lifespan</li>                    
                </ul>                              
            </td>
            <td style="text-align: left;"> People given treatment are [X.XX] times as likely to have positive endpoint compared to people not given treatment  </td>
        </tr>                                 
    </tbody>
</table>

By inverting outcomes that directionally deviate from the above standardized approach, we are able to report Effect Sizes in a consistent a manner. 
