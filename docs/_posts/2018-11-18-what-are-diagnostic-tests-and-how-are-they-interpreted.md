---
layout: post
title: What Are Diagnostic Tests And How Are They Interpreted?   
description: An overview of diagnostic tests and the various measures of interpretation, including predictive values, likelihood ratios, and odds ratios 
tags: Diagnostic_Tests Likelihood_Ratio Diagnostic_Odds_Ratio
---

{% include image.html name="header_21_resized.jpg" alt="What Are Diagnostic Tests And How Are They Interpreted" class="header-image" %} 

<p style="color: grey"><i>An overview of diagnostic tests and the various measures of interpretation, including predictive values, likelihood ratios, and odds ratios</i></p>


<!--more-->

Diagnostic tests are utilized to determine whether or not a patient has a particular disease.  The results of a given diagnostic test are traditionally [summarized](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2636062/) using four key parameters: 

<table>
    <thead>
        <tr>
            <th style="text-align: left;"></th>
            <th style="text-align: left;">Disease Present</th>
            <th style="text-align: left;">Disease Absent</th>                 
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="text-align: left;"><b>Positive</b></td>
            <td style="text-align: left;"><p>
                <b>True Positive (TP):</b>
                Patient has disease and test is positive                
            </p></td>
            <td style="text-align: left;"><p>
                <b>False Positive (FP):</b>
                Patient does not have disease but test is positive                
            </p></td>            
        </tr>
        <tr>
            <td style="text-align: left;"><b>Negative</b></td>
            <td style="text-align: left;"><p>
                <b>False Negative (FN):</b>
                Patient has disease but test is negative                
            </p></td>
            <td style="text-align: left;"><p>
                <b>True Negative (TN):</b>
                Patient does not have disease and test is negative                
            </p></td>   
        </tr>                                                        
    </tbody>
</table>

These parameters provide a window into the accuracy of the test, and building-blocks to derive a series of performance metrics:

<table>
    <thead>
        <tr>
            <th style="text-align: left;">Term</th>
            <th style="text-align: left;">Formula</th>
            <th style="text-align: left;">Definition</th>                 
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="text-align: left;"><b>Sensitivity</b></td>
            <td style="text-align: left;">TP / (TP+TN)</td>
            <td style="text-align: left;">Ability to detect the target disease when it does exist</td>
        </tr>
        <tr>
            <td style="text-align: left;"><b>Specificity</b></td>
            <td style="text-align: left;">TN / (TN+FP)</td>
            <td style="text-align: left;">Ability to not detect the target disease when it doesn't exist</td>
        </tr>
        <tr>
            <td style="text-align: left;"><b>Positive Predictive Value (PPV)</b></td>
            <td style="text-align: left;">TP / (TP+FP)</td>
            <td style="text-align: left;">Probability of having the target condition given a positive test result</td>
        </tr>
        <tr>
            <td style="text-align: left;"><b>Negative Predictive Value (NPV)</b></td>
            <td style="text-align: left;">TN / (FN+TN)</td>
            <td style="text-align: left;">Probability of not having the target condition given a negative test result</td>
        </tr>
        <tr>
            <td style="text-align: left;"><b>Positive Likelihood Ratio</b></td>
            <td style="text-align: left;">Sensitivity / (1 - Specificity)</td>
            <td style="text-align: left;">How much more likely a patient with the target disease will receive a positive test result compared to patients without the disease</td>
        </tr>
        <tr>
            <td style="text-align: left;"><b>Negative Likelihood Ratio</b></td>
            <td style="text-align: left;">(1 - Sensitivity) / Specificity</td>
            <td style="text-align: left;">How much more likely a patient with the target disease will receive a negative test result compared to patients without the disease</td>
        </tr>
        <tr>
            <td style="text-align: left;"><b>Diagnostic Odds Ratio</b></td>
            <td style="text-align: left;">(TP/FN) / (FP/TN)</td>
            <td style="text-align: left;">The ratio of the odds of a test being positive with subjects with a disease relative to the odds in subjects without disease </td>
        </tr>                                                                                                  
    </tbody>
</table>
