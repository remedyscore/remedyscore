---
layout: post
title: How Do We Summarize A Diagnostic Test's Effectiveness Using Area Under The Curve For A Single Study?   
description: An overview of using area under the curve to understand the effectiveness of a diagnostic test within a single study
tags: Diagnostic_Tests Diagnostic_Odds_Ratio Area_Under_Curve
---

{% include image.html name="header_24_resized.jpg" alt="How Do We Summarize A Diagnostic Test's Effectiveness Using Area Under The Curve For A Single Study" class="header-image" %} 

<p style="color: grey"><i>An overview of using area under the curve to understand the effectiveness of a diagnostic test within a single study</i></p>


<!--more-->

Area Under The Curve (AUC) measures a diagnostic test's accuracy by estimating the probability that a randomly chosen individual is correctly classified as diseased or disease-free.  The AUC can also be interpreted as an average sensitivity for the test, taken over all specificity values (or equally as the average specificity over all sensitivity values).

When creating an AUC for a single diagnostic study, data is usually tabulated based on three factors:

* **Sensitivity:**  Composed of True Positive and True Negative values

* **Specificity:**  Composed of False Positive and True Negative values

* **Cutpoint/Cut-Off/Threshold/Criterion:**  The test score the determines whether or not a patient is diseased or disease-free

So each row of a table will contemplate the Sensitivity/Specificity at a specific [Cutpoint](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3755824/) for the given study:

<table>
    <thead>
        <tr>
            <th style="text-align: left;">Cutpoint</th>
            <th style="text-align: center;">Sensitivity</th>
            <th style="text-align: center;">Specificity</th>                 
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="text-align: left;"><b>95</b></td>
            <td style="text-align: center;">98.18</td>
            <td style="text-align: center;">37.78</td>            
        </tr>           
        <tr>
            <td style="text-align: left;"><b>104</b></td>
            <td style="text-align: center;">94.55</td>
            <td style="text-align: center;">73.33</td>            
        </tr>  
        <tr>
            <td style="text-align: left;"><b>109</b></td>
            <td style="text-align: center;">90.91</td>
            <td style="text-align: center;">91.11</td>            
        </tr>                                                               
    </tbody>
</table>

On a more granular patient-level, consider the following example with different Cutpoints (green scores are considered healthy, and red scores are considered diseased): 
 
<table>
    <thead>
        <tr>
            <th style="text-align: left;">Patient</th>
            <th style="text-align: center;">Test Scores (95 Cutpoint)</th>
            <th style="text-align: center;">Test Scores (104 Cutpoint)</th>
            <th style="text-align: center;">Test Scores (109 Cutpoint)</th>                 
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="text-align: left;">1</td>
            <td style="text-align: center; background-color: #EAFAF1;">126.3</td>
            <td style="text-align: center; background-color: #EAFAF1;">126.3</td>
            <td style="text-align: center; background-color: #EAFAF1;">126.3</td>            
        </tr>           
        <tr>
            <td style="text-align: left;">2</td>
            <td style="text-align: center; background-color: #EAFAF1;">112.7</td>
            <td style="text-align: center; background-color: #EAFAF1;">112.7</td>
            <td style="text-align: center; background-color: #EAFAF1;">112.7</td> 
        </tr>  
        <tr>
            <td style="text-align: left;">3</td>
            <td style="text-align: center; background-color: #EAFAF1;">104.0</td>
            <td style="text-align: center; background-color: #EAFAF1;">104.0</td>
            <td style="text-align: center; background-color: #FDEDEC;">104.0</td>            
        </tr>
        <tr>
            <td style="text-align: left;">4</td>
            <td style="text-align: center; background-color: #EAFAF1;">97.9</td>
            <td style="text-align: center; background-color: #FDEDEC;">97.9</td>
            <td style="text-align: center; background-color: #FDEDEC;">97.9</td>            
        </tr>   
        <tr>
            <td style="text-align: left;">5</td>
            <td style="text-align: center; background-color: #FDEDEC;">94.9</td>
            <td style="text-align: center; background-color: #FDEDEC;">94.9</td>
            <td style="text-align: center; background-color: #FDEDEC;">94.9</td>            
        </tr>   
        <tr>
            <td style="text-align: left;">6</td>
            <td style="text-align: center; background-color: #FDEDEC;">92.8</td>
            <td style="text-align: center; background-color: #FDEDEC;">92.8</td>
            <td style="text-align: center; background-color: #FDEDEC;">92.8</td>            
        </tr> 
        <tr>
            <td style="text-align: left;"><b>Results</b></td>
            <td style="text-align: center;">
                <p><b>Sensitivity:</b> 98.2</p>
                <p><b>Specificity:</b> 37.8</p>
            </td>
            <td style="text-align: center;">
                <p><b>Sensitivity:</b> 94.6</p>
                <p><b>Specificity:</b> 73.3</p>
            </td>
            <td style="text-align: center;">
                <p><b>Sensitivity:</b> 90.9</p>
                <p><b>Specificity:</b> 91.1</p>
            </td>           
        </tr>                                                                                                 
    </tbody>
</table>

 
 
The Cutpoint is important, [because](http://gim.unmc.edu/dxtests/ROC1.htm) True Positives, False Negatives, False Positives, and True Negatives are classified based on the Cutpoint, which effectively dictates whether or not a patient is diseased.  When patients score close to this Cutpoint, changing it slightly can make the difference between counting that patient as a True Positive vs. False Positive or True Negative vs. False Negative (again, whether the patient is diseased or not).  

{% include image.html name="cutpoint_diagram.jpg" alt="Cutpoint Diagram" class="header-image" %}
 
For example, notice how a range of Cutpoints can change a given study's Sensitivity, Specificity, and number of Diseased/Disease-Free Patients: 

{% include image.html name="cutpoint_range.jpg" alt="Cutpoint Range" class="header-image" %} 

So, we see that by sensitizing around a Cutpoint (incrementing and decrementing it), various TP/FP/TN/FN values [are generated](https://www.medcalc.org/manual/roc-curves.php), and subsequently different Sensitivity/Specificity values are generated.  When plotting these Sensitivity/Specificity points on a Receiver Operating Characteristic ("ROC") graph with an x-axis of "(1 - Specificity)" (False Positive Rate) and a y-axis of "Sensitivity" (True Positive Rate), a curve is generated.  

{% include image.html name="area_under_curve.jpg" alt="Area Under Curve" class="header-image" %} 

The curve typically points to the top-left corner (where Sensitivity is 100% and Specificity is 100%).  

* The closer the curve moves towards the top-left corner the greater the amount of undisturbed area exists on the graph - and ultimately, the closer the test is to perfection.  

* This implies that a curve with a very large amount of area underneath it (less space taken on the graph / pressed in the top-left corner) - is a very effective test (high Sensitivity and Specificity); 

* Therefore, also implying that Diagnostic Tests with a large or high "Area Under the Curve" or AUC are desirable (particularly compared to a Diagnostic Test with a lower AUC)

Once a ROC has been graphed, it can also be used to [derive an optimal Cutpoint](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3755824/) among the plotted values:

<table>
    <thead>
        <tr>
            <th style="text-align: left;">Measurement</th>
            <th style="text-align: left;">Cutpoint Derived</th>
            <th style="text-align: left;">Formula</th>                 
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="text-align: left;">Distance To Top-Left Corner (Lower Is Better)</td>
            <td style="text-align: left;">Point closest to the top-left corner of the ROC curve</td>
            <td style="text-align: left;">SQRT( [ 1 - Sensitivity ]^2 + [ 1 - Specificity ]^2 )</td>            
        </tr>           
        <tr>
            <td style="text-align: left;">Youden Index (Higher is Better)</td>
            <td style="text-align: left;">Point on ROC curve farthest from a diagnosis being completely chance (50/50 guess / a diagonal line dividing graph in two)</td>
            <td style="text-align: left;">Sensitivity + Specificity – 1</td>            
        </tr>                                                              
    </tbody>
</table>

As indicated above, this value is approximated by finding the point (a) closest to the top-left corner or (b) farthest from the mid-point of the graph. 
