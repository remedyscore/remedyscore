---
layout: post
title: How Is An Effect Size Calculated For Dichotomous Data?   
description: An overview of calculating and interpreting an effect size for dichotomous data including risk and odds ratios
tags: Effect_Sizes Dichotomous_Data 
---

{% include image.html name="header_11_resized.jpg" alt="How Is An Effect Size Calculated For Dichotomous Data" class="header-image" %} 

<p style="color: grey"><i>An overview of calculating and interpreting an effect size for dichotomous data including risk and odds ratios</i></p>


<!--more-->

## OVERVIEW:

When a study contains Dichotomous Data (binary data, such as dead or alive, cured or not cured, etc.), an Odds Ratio or Risk Ratio is typically calculated as the effect size.  Generally speaking, the notion of a Risk Ratio is often easier to understand for people than an Odds Ratios.

## RISK RATIOS:  

A Risk Ratio is calculated by dividing the risk of the intervention group by the risk in the control group, where risk describes the probability that a particular health outcome will occur (the risk of a medication causing a headache is 25%).  For example, a Risk Ratio might be calculated as:
  
  (Intervention Headache / Total Subjects Tested) / (Control Headache / Total Subjects Tested)

When calculating the Risk Ratio, it is common to calculate it on a logarithmic scale.  This helps calculated results maintain a certain level of symmetry, for example consider: 
*  **Group A (Treatment Doubles Control):**    (10/100) / (5/100)  = 2.00
*  **Group B (Control Doubles Treatment):**    (5/100) / (10/100)  = 0.50

Intuitively, the combined Risk Ratio of Group A and Group B should cancel out and be equivalent to 1.00, but instead the mean is 1.25.  To derive more symmetrical results, it is common to take the natural logarithm of the calculated Risk Ratio and receive -0.693 (LN(0.50)) and +0.693 (LN(2.00)); which has the expected mean of 1.00.   These results are often referred to as the **Log Risk Ratio**.   

## ODDS RATIOS:

An Odds Ratio is calculated by dividing the odds of the intervention group by the odds in the control group, where odds describes the probability of that a particularly health outcome occurs compared to this outcome not occurring (the odds of having a headache from a medication were that one person had a headache for every three people that didn't).  For example, an Odds Ratio might be calculated as: 

(Intervention Headache / Intervention No Headache) / (Control Headache / Control No Headache)

In the same manner as the Risk Ratio, it is also common to the take the natural logarithm of an Odds Ratio, in order to derive a more symmetrical **Log Odds Ratio**.

## INTERPRETING RESULTS:

The output of calculating a Risk Ratio or Odds Ratio can be interpreted as follows:

<table>
    <thead>
        <tr>
            <th style="text-align: left;">Dichotomous Data</th>
            <th style="text-align: left;">Risk Ratio Interpretation</th>
            <th style="text-align: left;">Odds Ratio Interpretation</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="text-align: left;">
                <p><b>Odds / Risk Ratio > 1</b></p>
                <p><b>(Treatment > Control)</b></p>
                <p>Outcome is more likely to occur in the treatment group when compared to the control group</p>
            </td>
            <td style="text-align: left;">For example, a risk ratio of 1.79 means the intervention increased the risk of having a headache by 79%</td>
            <td style="text-align: left;">For example, a risk ratio of 2.06 means the intervention increased the odds of having a headache by 106%</td>
        </tr>  
        <tr>
            <td style="text-align: left;">
                <p><b>Odds / Risk Ratio = 1</b></p>
                <p><b>(Treatment = Control)</b></p>
                <p>No difference between the treatment and control group</p>
            </td>
            <td style="text-align: left;">For example, a risk ratio of 1.00 means the intervention did not increase or decrease the risk of having a headache</td>
            <td style="text-align: left;">For example, an odds ratio of 1.00 means the intervention did not increase or decrease the odds of having a headache</td>
        </tr>  
        <tr>
            <td style="text-align: left;">
                <p><b>Odds / Risk Ratio < 1</b></p>
                <p><b>(Treatment < Control)</b></p>
                <p>Outcome is less likely to occur in the treatment group when compared to the control group</p>
            </td>
            <td style="text-align: left;">For example, a risk ratio of 0.79 means the intervention reduced the risk the of having a headache by 21%</td>
            <td style="text-align: left;">For example, an odds ratio of 0.06 means the intervention reduced the odds the of having a headache by 94%</td>
        </tr>                                     
    </tbody>
</table>
