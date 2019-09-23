---
layout: post
title: How Do We Summarize A Diagnostic Test's Effectiveness Using Area Under The Curve For Multiple Studies?   
description: An overview of using area under the curve to understand the effectiveness of a diagnostic test for multiple studies
tags: Diagnostic_Tests Diagnostic_Odds_Ratio Area_Under_Curve
---

{% include image.html name="header_25_resized.jpg" alt="How Do We Summarize A Diagnostic Test's Effectiveness Using Area Under The Curve For Multiple Studies" class="header-image" %} 

<p style="color: grey"><i>An overview of using area under the curve to understand the effectiveness of a diagnostic test for multiple studies</i></p>


<!--more-->

The concept of determining an Area Under the Curve (AUC) can be applied to multiple studies by simply graphing each study's:

* (1 - Specificity) or the False Positive Rate; and
 
* Sensitivity or the True Positive Rate

The only difference from a single study is that each data-point naturally originates from [a different study](https://www.annalsthoracicsurgery.org/article/S0003-4975(04)01986-1/fulltext), and not a different Cutpoint.  This implies that every plotted study has a similar Cutpoint (evaluation criteria for diseased or disease-free), so varying Cutpoints are not influencing the shape of the curve (and therein area underneath it).  

The resultant graph that is produced from plotting multiple studies is called a Summary Receiver Operating Characteristic ("SROC").  In order to create a SROC with a reasonable chance of being normally distributed, it is assumed that at least [ten studies](https://www.annalsthoracicsurgery.org/article/S0003-4975(04)01986-1/fulltext) have been plotted.  Studies that plot as outliers should also be assessed for validity, and particular caution should be taken when said studies have populations less than thirty.

As with any meta-analysis that combines studies, a SROC [does not account for](https://www.annalsthoracicsurgery.org/article/S0003-4975(04)01986-1/fulltext) variability in patient population, physician experience and training, and environmental characteristics.   

While AUC calculations were initially based upon the aforementioned SROC curve - these curves since added a 'hierarchical' component to create a HSROC curve.  The hierarchical component was included because SROC curves [often](http://imohw.tmu.edu.tw/idohtmu/wp-content/uploads/2015/11/20151023_3-Introduction-to-DTA-meta-analysis.pdf) underestimate test accuracy due to (a) bias in weights and (b) sampling variability.

* **HSROC Model:**  As a result, a hierarchical model was developed to avoid unnecessary weighting adjustments; and account for both within (sampling error) and between study variability (through random effects).   The resultant HSROC model analyzes given data-points and produces a Curve Summary based on the HSROC curve's accuracy, shape, and threshold/cutpoints.

* **Bivariate Model:**  It is also possible to mitigate the deficiencies of the SROC curve - and largely mirror the HSROC model - using Bivariate modeling.  The primary difference is that a Bivariate model focuses on a Point Summary (not a Curve Summary) - which is derived from given sensitivities, specificities, and the correlation between them. 

Visually speaking, the difference between these models can be seen [as follows](https://www.sciencedirect.com/science/article/pii/S1198743X14600434):

{% include image.html name="hsroc_bivariate.jpg" alt="HSROC Bivariate" class="header-image" %} 

Note that both models (HSROC and Bivariate) also produce equivalent results in [the](https://academic.oup.com/biostatistics/article/8/2/239/230328) [absence of any covariates](https://www.ncbi.nlm.nih.gov/books/NBK98250/). 

In general, the HSROC Model is [recommended](https://www.sciencedirect.com/science/article/pii/S1198743X14600434) when meta-analyzing studies with different thresholds for test positivity, and the Biviarate Model is recommended when meta-analyzing studies with similar thresholds for test positivity.  The reason for this is that the HSROC Model considers a threshold as a factor when deriving an AUC - so it can account for threshold variability (advantage) - but will fail to derive meaningful results when thresholds are all similar (disadvantage). 

The above being said, there are primarily two methods of performing Bivariate Modeling: 

* **Reitsma Model:**  [Reitsma](http://www.jclinepi.com/article/S0895-4356(05)00162-9/fulltext) provided an initial Bivariate model that has become [standardized](https://stats.stackexchange.com/questions/203745/which-is-the-best-method-for-meta-analysis-of-diagnostic-test-accuracy-studies) with the '[mada](https://www.rdocumentation.org/packages/mada/versions/0.5.8)' [R package](https://cran.r-project.org/web/packages/mada/index.html) and is frequently used when calculating diagnostic test accuracy within a meta-analysis.

* **Proportional Hazards Model (PHM):**  Holling has subsequently developed a Proportional Hazards Model (PHM) that [rectifies](http://www.personal.soton.ac.uk/dab1f10/psychomethods2012.pdf) the HSROC model's usage of a logit transformation that fails to account for a limited amount of data and avoids skewed results.  PHM has a [track-record](https://www.nature.com/articles/srep29325#f2) of being used to assess AUC (Nobuyuki Horita has conducted numerous meta-analyses that favor PHM over Reitsma when calculating AUC), and is utilized within RemedyScore for similar purposes.

When generating an Area Under The Curve (AUC) value from these models, the result's [performance](https://www.omicsonline.org/evaluating-measures-of-indicators-of-diagnostic-test-performance-fundamental-meanings-and-formulars-2155-6180.1000132.php?aid=4054) [can](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4975285/) [be](http://gim.unmc.edu/dxtests/roc3.htm) [evaluated](http://methods.cochrane.org/sites/methods.cochrane.org.sdt/files/public/uploads/Chapter%2010%20-%20Version%201.0.pdf) [as](http://wixtedlab.ucsd.edu/publications/Psych%20218/Swets_1988.pdf) [follows](https://www.annalsthoracicsurgery.org/article/S0003-4975(04)01986-1/fulltext):

<table>
    <thead>
        <tr>
            <th style="text-align: left;">Category</th>
            <th style="text-align: left;">Performance</th>                             
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="text-align: left;"><p><b>No Performance /</b></p> <p><b><a href="https://www.sciencedirect.com/science/article/pii/S008525381553963X">Erroneous Data</a></b></p></td>
            <td style="text-align: left;">0.00 - 0.50</td>
        </tr>           
        <tr>
            <td style="text-align: left;"><b>Low Performance</b></td>
            <td style="text-align: left;">0.50 - 0.70</td>
        </tr>   
        <tr>
            <td style="text-align: left;"><b>Medium Performance</b></td>
            <td style="text-align: left;">0.70 - 0.90</td>
        </tr>   
        <tr>
            <td style="text-align: left;"><b>High Performance</b></td>
            <td style="text-align: left;">0.90 - 1.00</td>
        </tr>                                                                               
    </tbody>
</table>

This means a result of 1.00 equals a perfect test and anything below 0.5 is a completely uninformative test.  For example, an AUC of 0.89 suggests an 89% chance that a disease will be correctly diagnosed.  

The above being said, RemedyScore utilizes a more conservative range for interpreting AUC values, which is also consistent with measures applied to Diagnostic Odds Ratios.  This range is as follows:

<table>
    <thead>
        <tr>
            <th style="text-align: left;">Category</th>
            <th style="text-align: left;">Performance</th>                             
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="text-align: left;"><p><b>No Performance /</b></p><p><b>Erroneous Data</b></p></td>
            <td style="text-align: left;">0.00 - 0.50</td>
        </tr>           
        <tr>
            <td style="text-align: left;"><b>Low Performance</b></td>
            <td style="text-align: left;">0.50 - 0.90</td>
        </tr>   
        <tr>
            <td style="text-align: left;"><b>Medium Performance</b></td>
            <td style="text-align: left;">0.90 - 0.96</td>
        </tr>   
        <tr>
            <td style="text-align: left;"><b>High Performance</b></td>
            <td style="text-align: left;">0.96 - 1.00</td>
        </tr>                                                                               
    </tbody>
</table>
