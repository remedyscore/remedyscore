---
layout: post
title: What Types Of Studies Should Be Avoided In A Meta-Analysis?   
description: An overview of studies that should be avoided when performing a meta-analysis
tags: Medical_Studies Meta_Analysis Cross_Over_Trials 
---

{% include image.html name="header_10_resized.jpg" alt="What Types Of Studies Should Be Avoided In A Meta-Analysis" class="header-image" %} 

<p style="color: grey"><i>An overview of studies that should be avoided when performing a meta-analysis</i></p>


<!--more-->

The most common type of clinical study is a **Parallel Group Trial**, wherein two groups of participants are divided into an intervention and control group.  For example, Group A receives the control and Group B is receives the intervention.  This is the most ideal type of randomized trial to review in a meta-analysis.

That being said, many other types of studies are less desirable for inclusion in a meta-analysis, including:
 
* **Cross-Over Trials:**  All participants receive the same intervention.  For example, Group A receives the control and then the intervention, and Group B receives the intervention and then the control.  Cross-over studies are a fairly unique form of study that appears in roughly [15%](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0133023) of medical trials. As opposed to a standard parallel study, a cross-over study gives participants both a placebo and active treatment in a random order, interspersed with a wash-out period; for example:

<table>
    <thead>
        <tr>
            <th style="text-align: left;">Group</th>
            <th style="text-align: center;">Phase 1</th>
            <th style="text-align: center;">Wash-Out</th>
            <th style="text-align: center;">Phase 2</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="text-align: left;"><b>Group 1</b></td>
            <td style="text-align: center;">Treatment</td>
            <td style="text-align: center;">-</td>
            <td style="text-align: center;">Placebo</td>
        </tr>  
        <tr>
            <td style="text-align: left;"><b>Group 2</b></td>
            <td style="text-align: center;">Placebo</td>
            <td style="text-align: center;">-</td>
            <td style="text-align: center;">Treatment</td>
        </tr>                       
    </tbody>
</table>
  
Cross-over studies have a variety of advantages and disadvantages:  

<table>
    <thead>
        <tr>
            <th style="text-align: left;">#</th>
            <th style="text-align: left;">Advantages</th>
            <th style="text-align: left;">Disadvantages</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="text-align: left;">1</td>
            <td style="text-align: left;">Only requires half the number of patients as parallel studies</td>
            <td style="text-align: left;">Takes more than twice as long as parallel studies, because patients receive both the placebo and treatment, as well as a 'wash-out' period in between both phases</td>
        </tr>  
        <tr>
            <td style="text-align: left;">2</td>
            <td style="text-align: left;">Provides more precise results because a study is comparing the same patient's responses to both a placebo and treatment (patients act as their own control)</td>
            <td style="text-align: left;">Drug effects may 'carry-over' from one phase to another, despite a wash-out period - making a patient more susceptible to particular outcomes</td>
        </tr> 
        <tr>
            <td style="text-align: left;">3</td>
            <td style="text-align: left;"></td>
            <td style="text-align: left;">Patients also may gather information about the intended study during the initial phase altering the outcome of subsequent phases</td>
        </tr>                                
    </tbody>
</table>

Note that a cross-over study is inappropriate for testing treatments that may result in an irreversible change (curing a disease, pregnancy, etc.) as these treatments inherently remove patients from later phases of the study.

There are three options available for [analyzing](https://academic.oup.com/ije/article/31/1/140/655940) [cross-over studies](http://handbook-5-1.cochrane.org/chapter_16/16_4_5_methods_for_incorporating_cross_over_trials_into_a.htm), which trade ease of implementation for accuracy:
 
<table>
    <thead>
        <tr>
            <th style="text-align: left;">#</th>
            <th style="text-align: left;">Data Required</th>
            <th style="text-align: left;">Disadvantages</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="text-align: left;"><b>1</b></td>
            <td style="text-align: left;"><b>Within-Patient Differences for Both Phases</b></td>
            <td style="text-align: left;">
                <p> <b>Continuous Data:</b> Utilize within-patient differences for the mean and standard deviation and calculate a paired analysis by <a href="http://handbook-5-1.cochrane.org/chapter_16/16_4_5_methods_for_incorporating_cross_over_trials_into_a.htm">imputing</a> <a href="http://handbook-5-1.cochrane.org/chapter_16/16_4_6_4_example.htm">missing</a> <a href="https://academic.oup.com/ije/article/31/1/140/655940">standard</a> deviations via a correlation coefficient derived from similar studies.</p> 
                <p> <b>Dichotomous Data:</b> Often require <a href="https://academic.oup.com/ije/article/31/1/140/655940">complex</a> statistics to calculate a paired analysis and is generally <a href="http://handbook-5-1.cochrane.org/chapter_16/16_4_5_methods_for_incorporating_cross_over_trials_into_a.htm">not recommended</a> </p>
            </td>
        </tr>  
        <tr>
            <td style="text-align: left;"><b>2</b></td>
            <td style="text-align: left;"><b>Patient Data for Each Phase</b></td>
            <td style="text-align: left;">Use the first phase as a miniature parallel study, accepting that information in the second phase of the study will be discarded.   Note that this approach can be beneficial when a study's wash-out period is deemed insufficient and there is a risk of carry-over between phases.  To that point, when data is presented in this manner – carefully check the study to ensure that there isn't any carry-over risk – because authors often present data in this manner when such a risk appears.</td>
        </tr> 
        <tr>
            <td style="text-align: left;"><b>3</b></td>
            <td style="text-align: left;"><b>Patient Data for Each Phase</b></td>
            <td style="text-align: left;">Treat both phases as separate parallel studies. Unfortunately, this neglects that the same patients are in both phases of the study, and have some level of statistical dependency.  Consequently, the resultant confidence intervals will likely be too wide, the trial will receive too little weight, and potentially disguise the amount of heterogeneity. </td>
        </tr>                                
    </tbody>
</table>


Given the complexity of performing the above analysis, it is little surprise that nearly [70% of cross-over studies](https://pdfs.semanticscholar.org/c7ec/45d8d6689baf98136f60e2fe75f36e5dc2f3.pdf) are excluded from meta-analyses.  In general, however, the second option presented above is likely the best balance between complexity and accuracy - but even then, there is a [general notion](http://handbook-5-1.cochrane.org/chapter_16/16_4_7_issues_in_the_incorporation_of_cross_over_trials.htm) that inclusion of cross-over studies should be done with care.  This means performing a sensitivity analysis that separates parallel studies from cross-over studies to investigate the robustness of any conclusions.

* **Clustered Trials:**  Groups of people – often based on similar characteristics, such as being from the same clinics, schools, or geographies – are selected to receive either the control or intervention.  For example, Clinic A receives the control and Clinic B receives the intervention.  This type of trial is not viewed as truly randomized (due to populations having similar characteristics), and is not ideal for a systematic review. 

* **Open-Label Extension Studies:**  Enrollment into an open-label extension study typically follows enrollment into a randomized, blinded, well-controlled main study.  Participants are usually informed at the time they are recruited into the main study that they may elect to enroll in an open-label extension study after completing the main trial.  Open-label extension studies are typically conducted to observe the long-term safety of a treatment and any adverse effects that may appear.  Unfortunately: 

  * Most adverse effects have already been detected in the initial clinical trial, providing very little additional insight beyond refining data; and
  
  * The study is conducted in an uncontrolled and biased manner, consequently making said data less valuable.  [For example](http://www.appliedclinicaltrialsonline.com/spotlight-open-label-extension-studies), even if an adverse effect appears during the open-label extension study, without a control-group this effect could be blamed on the disease, another affliction, or concomitant therapies. 

  As such it is rare for a meta-analysis to include data on an open-label extension study, since it is preferable to simply include data from the original trial which featured a randomized control group (placebo).  At best, a meta-analysis may discuss an open-label extension study within the narrative of the review – but this is likely the extent the study will appear in the analysis.

* **Non-Randomized Trials:** These trials are not randomized, and should be excluded due to their testing methodology 
