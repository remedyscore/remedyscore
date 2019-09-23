---
layout: post
title: How Are Diagnostic Tests' Effectiveness Summarized Using Odds Ratios?   
description: An overview of diagnostic odds ratios and how they might be interpreted to determine the significance of an intervention
tags: Diagnostic_Tests Diagnostic_Odds_Ratio Area_Under_Curve
---

{% include image.html name="header_23_resized.jpg" alt="How Are Diagnostic Tests' Effectiveness Summarized Using Odds Ratios" class="header-image" %} 

<p style="color: grey"><i>An overview of odds ratios and how they might be interpreted to determine the significance of an intervention</i></p>


<!--more-->

As established previously, Likelihood Ratios are useful for assessing the Sensitivity and Specificity of a given diagnostic test.  Unfortunately, both the Positive and Negative Likelihood Ratio must be reviewed before drawing conclusions about a specific test.  Ideally, it would be desirable to have a single metric for assessing a diagnostic test's overall effectiveness.  The Diagnostic Odds Ratio ("DOR") provides this single metric, as [it expresses](http://www.scielo.br/scielo.php?pid=s0066-782x2009000300013&script=sci_arttext&tlng=en) the Positive Likelihood Ratio divided by the Negative Likelihood Ratio.  It also functions in a very [similar](http://www.scielo.br/scielo.php?pid=s0066-782x2009000300013&script=sci_arttext&tlng=en) [manner](http://www.archivesofpathology.org/doi/pdf/10.5858/arpa.2011-0016-SO?code=coap-site) to a standard Odds Ratio calculated when analyzing randomized controlled trials with Dichotomous Data.

The Diagnostic Odds Ratio can be calculated as follows:

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
            <td style="text-align: left;"><b>Diagnostic Odds Ratio</b></td>
            <td style="text-align: left;">(TP/FN) / (FP/TN)</td>
            <td style="text-align: left;">The ratio of the odds of a test being positive with subjects with a disease relative to the odds in subjects without disease </td>            
        </tr>                                                        
    </tbody>
</table>

The same logic used to perform a meta-analysis for a standard Odds Ratio can be applied to a Diagnostic Odds Ratio:

<table>
    <thead>
        <tr>
            <th style="text-align: left;"></th>
            <th style="text-align: left;">Events</th>
            <th style="text-align: left;">Non-Events</th>                 
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="text-align: left;"><b>Treatment</b></td>
            <td style="text-align: left;">True Positive</td>
            <td style="text-align: left;">False Negatives</td>            
        </tr>
        <tr>
            <td style="text-align: left;"><b>Control</b></td>
            <td style="text-align: left;">False Positives</td>
            <td style="text-align: left;">True Negatives</td>            
        </tr>                                                                
    </tbody>
</table>

From these values, a [Log Odds Ratio](https://en.wikipedia.org/wiki/Diagnostic_odds_ratio#Uses) and Variance value can be computed and passed into a typical Meta-Analysis framework for calculation: 

Log Odds Ratio = LN [ (True Positive x True Negative) / (False Negative x False Positive) ]

Note that: 

* Due to expected heterogeneity between studies, a Random Effects Model is always used when performing a meta-analysis of diagnostic tests (sometimes called "pooling" the results).  A Fixed Effects Model should only be used when there are numerically too few studies to estimate a "Between Study Variance". 

* When [calculating](https://pdfs.semanticscholar.org/abdc/2e0d212d71f0c3349025a8efdff755cc8b1c.pdf) the DOR (or any Odds Ratio), when any input has a zero value, increment all inputs 0.5 to avoid a divide by zero error

Note the following when interpreting the results of a given DOR:

* A DOR can [range](https://pdfs.semanticscholar.org/abdc/2e0d212d71f0c3349025a8efdff755cc8b1c.pdf) between zero to infinity, with one meaning the test fails to discriminate between patients with and without a disease.

* A DOR can be [calculated](http://methods.cochrane.org/sites/methods.cochrane.org.sdt/files/public/uploads/DTA%20Handbook%20Chapter%2011%20201312.pdf) using different Sensitivity and Specificity combinations - for example, a DOR of 9 could be  achieved by a Specificity of 90% and a Sensitivity of 50% or by a Sensitivity of 50% and a Specificity of 90%.

* For this reason, a DOR is [not recommended](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4644739/) as an outcome index for a meta-analysis, [when](https://www.academia.edu/12945538/The_diagnostic_odds_ratio_a_single_indicator_of_test_performance) [the](https://www.ncbi.nlm.nih.gov/books/NBK98250/) balance between false negative and false positive rates is of importance

* Put differently, a DOR value in isolation [does not](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4644739/) distinguish between the ability to detect diseased cases (Sensitivity) and the ability to detect non-diseased cases (Specificity); it is an aggregate number

The above being said, given that the DOR is effectively a ratio of Specificity and Sensitivity - any given DOR can be plotted graphically as follows:

{% include image.html name="auc_dor.png" alt="Area Under Curve Diagnostic Odds Ratio" class="header-image" %}

The above curve visually demonstrates multiple Sensitivity/Specificity combinations can equate to a single DOR.

For example, a DOR of 21 might be composed of the following Sensitivity/Specificity combinations:

* 0.70 Sensitivity, 0.90 Specificity

* 0.82 Sensitivity, 0.82 Specificity 

* 0.90 Sensitivity, 0.70 Specificity 

When plotted to create a DOR curve, Sensitivity/Specificity combinations allows a reader to visually assess a test's accuracy by locating the point plotted in the upper-left corner (for example, 0.82, 0.82).  This point can then be compared to a 'perfect test', which would include a 1.00 Sensitivity and 1.00 Specificity, and have a point that resides in the absolute upper-left corner of the graph. 

The DOR's a close relationship to the Positive and Negative Likelihood Ratio can be seen formulaically as:

Diagnostic Odds Ratio = Positive Likelihood Ratio / Negative Likelihood Ratio 

[We can apply](https://www.researchgate.net/publication/7961154_A_methodological_review_of_how_heterogeneity_has_been_examined_in_systematic_reviews_of_diagnostic_test_accuracy) the same interpretation metrics we found with Likelihood Ratios to the Diagnostic Odds Ratio: 

**Positive Likelihood Ratio:** 

<table>
    <thead>
        <tr>
            <th style="text-align: left;">Value</th>
            <th style="text-align: left;">DOR</th>
            <th style="text-align: left;">Log DOR</th>
            <th style="text-align: left;">Change In Probability</th>
            <th style="text-align: left;">Qualitative Significance</th>                 
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="text-align: left;">> 10.00</td>
            <td style="text-align: left;">> 100</td>
            <td style="text-align: left;">> 4.6</td>
            <td style="text-align: left;">> 45%</td>
            <td style="text-align: left;">Large</td>                        
        </tr>
        <tr>
            <td style="text-align: left;">10.00 - 5.00</td>
            <td style="text-align: left;">100 - 25</td>
            <td style="text-align: left;">4.6 - 3.2</td>
            <td style="text-align: left;">45% - 30%</td>
            <td style="text-align: left;">Medium</td>                        
        </tr>  
        <tr>
            <td style="text-align: left;">< 5.00</td>
            <td style="text-align: left;">< 25</td>
            <td style="text-align: left;">< 3.2</td>
            <td style="text-align: left;"><30%</td>
            <td style="text-align: left;">Small</td>                        
        </tr>  
        <tr>
            <td style="text-align: left;">0.00</td>
            <td style="text-align: left;">1</td>
            <td style="text-align: left;">0</td>
            <td style="text-align: left;">0%</td>
            <td style="text-align: left;">None</td>                        
        </tr>                                                                               
    </tbody>
</table>

**Negative Likelihood Ratio:** 

<table>
    <thead>
        <tr>
            <th style="text-align: left;">Value</th>
            <th style="text-align: left;">DOR</th>
            <th style="text-align: left;">Log DOR</th>
            <th style="text-align: left;">Change In Probability</th>
            <th style="text-align: left;">Qualitative Significance</th>                 
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="text-align: left;">0.00</td>
            <td style="text-align: left;">1</td>
            <td style="text-align: left;">0</td>
            <td style="text-align: left;">0%</td>
            <td style="text-align: left;">None</td>                        
        </tr>     
        <tr>
            <td style="text-align: left;">> 0.05</td>
            <td style="text-align: left;">> 100</td>
            <td style="text-align: left;">> 4.6</td>
            <td style="text-align: left;">> -45%</td>
            <td style="text-align: left;">Large</td>                        
        </tr>
        <tr>
            <td style="text-align: left;">0.10 - 0.20</td>
            <td style="text-align: left;">100 - 25</td>
            <td style="text-align: left;">4.6 - 3.2</td>
            <td style="text-align: left;">-45% - -30%</td>
            <td style="text-align: left;">Medium</td>                        
        </tr>  
        <tr>
            <td style="text-align: left;">< 0.20</td>
            <td style="text-align: left;">< 25</td>
            <td style="text-align: left;">< 3.2</td>
            <td style="text-align: left;"><-30%</td>
            <td style="text-align: left;">Small</td>                        
        </tr>                                                                                
    </tbody>
</table>

For the purposes of determining a Diagnostic Odds Ratio (one thing divided by another thing) - the above Likelihood Ratios must be viewed as pairs:

* 100 (Diagnostic Odds Ratio) = 10.0 (Positive Likelihood Ratio) / 0.10 (Negative Likelihood Ratio); or

* 25 (Diagnostic Odds Ratio) = 5.0 (Positive Likelihood Ratio) / 0.20 (Negative Likelihood Ratio)

As one might imagine, inverting the relationship between Positive and Negative Likelihood Ratio (0.10 Positive / 10.0 Negative) produces a different - diametrically opposed - result.

Note that a Log DOR is typically [preferable](http://www.let.rug.nl/nerbonne/teach/rema-stats-meth-seminar/presentations/Lobanova-2008-OddsRatio.pdf) [when](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC1127651/) summarizing an Odds Ratio, because:

* It avoids any skewed distribution in sampling when analyzing small and moderate sample sizes

* It roughly has a normal distribution - so it can handle very small and large values in the same manner (as opposed to being constrained to zero on the lower end but having the ability to reach infinity on the upper end)
