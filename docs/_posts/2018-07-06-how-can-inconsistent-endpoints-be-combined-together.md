---
layout: post
title: How Can Inconsistent Endpoints Be Combined Together?   
description: An overview of endpoint inconsistencies and how they can be mitigated to still combine studies together
tags:  Endpoints Random_Effects_Model
---

{% include image.html name="header_9_resized.jpg" alt="How Can Inconsistent Endpoints Be Combined Together" class="header-image" %} 

<p style="color: grey"><i>An overview of endpoint inconsistencies and how they can be mitigated to still combine studies together</i></p>


<!--more-->

In an ideal world, researchers would develop and adopt a core set of endpoint measurements when testing a particular treatment.  Unfortunately, it is common to see clinical trials inconsistently select, measure, and report a given endpoint.  This can create a challenge when attempting to aggregate these endpoints within a meta-analysis. 

Examples of said inconsistencies might include:

<table>
    <thead>
        <tr>
            <th style="text-align: center;">#</th>
            <th style="text-align: left;">Inconsistency</th>
            <th style="text-align: left;">Study 1</th>
            <th style="text-align: left;">Study 2</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="text-align: center;"><b>1</b></td>
            <td style="text-align: left;">Selection</td>
            <td style="text-align: left;">Measures levels of pain in students at a particular university</td>
            <td style="text-align: left;">Measures levels of pain in an unaffiliated collection of geographically dispersed hospitals</td>
        </tr>  
        <tr>
            <td style="text-align: center;"><b>2</b></td>
            <td style="text-align: left;">Measurement</td>
            <td style="text-align: left;">Measures levels of pain by asking individuals to self-report their experiences</td>
            <td style="text-align: left;">Measures levels of pain by asking physicians to assess the behavior of their patients</td>
        </tr>  
        <tr>
            <td style="text-align: center;"><b>3</b></td>
            <td style="text-align: left;">Reporting</td>
            <td style="text-align: left;">Measures the number of patients that self-report at least a 30% decrease in pain</td>
            <td style="text-align: left;">Measures the number of patients that self-report at least a 50% decrease in pain</td>
        </tr>                           
    </tbody>
</table>

In the event that inconsistencies exist but ultimately have no impact on the results of each study, a meta-analysis [can be performed](http://handbook-5-1.cochrane.org/chapter_12/12_6_1_meta_analyses_with_continuous_outcomes.htm) without problem. 

However, when inconsistencies create fundamentally different levels of accuracy or outputs, an attempt to combine studies together can lead to substantial heterogeneity and [dilute any conclusions](https://www.meta-analysis.com/downloads/Intro_Criticisms_optim.pdf).  In some studies, that might be [combining](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5643683/) "[apples and oranges](http://bjp.rcpsych.org/content/bjprcpsych/200/6/446.full.pdf)".  To combat this problem, a few solutions exist:
 
* **Random Effects Model:**  When calculating an Effect Size, a Random Effects Model can help eliminate variability between studies that include inconsistencies (things like patient age, the size of an intervention, etc).  This is accomplished by decomposing the total variance of the study endpoints into (a) random sampling variance (Variance Within) and (b) systematic between study variance (Variance Between).  These two variance measures help refine: 

  * **Weights:**  [Even-out](https://pdfs.semanticscholar.org/c88e/8ff3f4cff6790a996576cc0c629332ff251a.pdf) the weights (which are based on variance), so large studies lose influence while small studies gain influence; and 

  * **Confidence Intervals:**  [Increase](https://www.meta-analysis.com/downloads/Meta-analysis%20Fixed-effect%20vs%20Random-effects%20models.pdf) the amount of variance (no longer just Variance Within; but Variance Within + Variance Between), which in turn widens the standard error and confidence interval for a given effect-size
The end-result is a more conservative view of a particular meta-analysis (compared to a Fixed Effects Model), which better takes into account the variability found in the studies being analyzed.  This variability is meant to mirror the assumption that the studies included in the given meta-analysis are just a random sample ("Random" Effects Model) of all possible studies that meet the inclusion criteria for the review.

* **Subgroup (Moderator) Analysis:**  Can be performed using meaningful [sub-groups](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3708764/) [collected during](http://www.ijaweb.org/article.asp?issn=0019-5049;year=2016;volume=60;issue=9;spage=689;epage=694;aulast=Sriganesh) the review.  Subgroups are often formed by observing clusters of studies with homogeneous results and identifying any common variables ("moderator variables").  By "coding" the study with these distinguishing variables (patient type, sample size, study duration, etc.) - one can decompose the meta-analysis into groups and observe the component effect sizes. 

* **Sensitivity Analysis:**  Can be [performed](http://handbook-5-1.cochrane.org/chapter_9/9_7_sensitivity_analyses.htm) on any over-arching effect size by removing sub-groupings and observing the impact on the effect size.  For example, if a particular subgroup has an outlying characteristic (patient age, dosage amount, short duration, etc.) - this can be removed to ensure that the effect size remains largely unchanged.  The net result is an assurance that effect size was not the product of poor decision making during the study selection process. 

The central point is that while studies may have inconsistencies - the more variability they introduce, the greater the chance that results will display high heterogeneity ('I^2') and limit confidence around any reported conclusions.  In this event, it might be necessary to break-up the study into logical components and move away from measuring "fruit" as whole - and into the component parts of "apple" and "orange".  A subgroup and sensitivity analysis can help guide the process of partitioning a study in this manner, if necessary.  
