---
layout: post
title: How Can Multiple Study Groups Be Combined Into A Single Study Group?   
description: An overview of combining together dichotomous and continuous study data
tags:  Meta_Analysis Dichotomous_Data Continuous_Data 
---

{% include image.html name="header_8_resized.jpg" alt="How Can Multiple Study Groups Be Combined Into A Single Study Group" class="header-image" %} 

<p style="color: grey"><i>An overview of combining together dichotomous and continuous study data</i></p>


<!--more-->

## OVERVIEW:

When performing a meta-analysis, it is not uncommon to see patients divided into different study groups by a unique differentiator such as: 

* Gender

* Dose-Response Measure (patients receiving 8mg, 16mg, or 32mg treatment)

* Geographic Location

While dividing patients into these groups may serve a purpose within an individual study, it can often be an artificial disaggregator when conducting a meta-analysis.  Fortunately, studies can be readily combined together based upon the type of data provided.  Note that these techniques do not address combining multiple, existing effect sizes - but rather multiple studies before any effect sizes have been calculated.

## DICHOTOMOUS DATA:

When analyzing dichotomous data, it is relatively easy to combine together studies: 

<table>
    <thead>
        <tr>
            <th style="text-align: left;">Treatment</th>
            <th style="text-align: center;">Events</th>
            <th style="text-align: center;">Non-Events</th>
            <th style="text-align: center;">Totals</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="text-align: left;"><b>Placebo</b></td>
            <td style="text-align: center;">19</td>
            <td style="text-align: center;">23</td>
            <td style="text-align: center;">42</td>
        </tr> 
        <tr>
            <td style="text-align: left;"><b>Dosage 1</b></td>
            <td style="text-align: center;">21</td>
            <td style="text-align: center;">21</td>
            <td style="text-align: center;">41</td>
        </tr>  
        <tr>
            <td style="text-align: left;"><b>Dosage 2</b></td>
            <td style="text-align: center;">24</td>
            <td style="text-align: center;">19</td>
            <td style="text-align: center;">43</td>
        </tr>  
        <tr>
            <td style="text-align: left;"><b>Dosage 3</b></td>
            <td style="text-align: center;">26</td>
            <td style="text-align: center;">18</td>
            <td style="text-align: center;">44</td>
        </tr>   
        <tr>
            <td style="text-align: left;"></td>
            <td style="text-align: center;"></td>
            <td style="text-align: center;"></td>
            <td style="text-align: center;"></td>
        </tr>   
        <tr style="background-color: #EEEEEE;">
            <td style="text-align: left;   background-color: #EEEEEE;"><b>Dosage 1+2+3</b></td>
            <td style="text-align: center; background-color: #EEEEEE;">71</td>
            <td style="text-align: center; background-color: #EEEEEE;">57</td>
            <td style="text-align: center; background-color: #EEEEEE;">128</td>
        </tr>                                     
    </tbody>
</table>

In the above example, we simply calculate the incidences of events for each dosage (study group) and add them together.  When percentages of specific events are given (50% of patients responded to Dosage 1, 55% of patients responded to Dosage 2, etc.) - the percentages can be multiplied by the total patient count and the number of events can be derived.

## CONTINUOUS DATA:

When analyzing continuous data, combining together studies becomes slightly more complicated.

We achieve the following results:

<table>
    <thead>
        <tr>
            <th style="text-align: left;">Treatment</th>
            <th style="text-align: center;">Mean</th>
            <th style="text-align: center;">Population</th>
            <th style="text-align: center;">Std Dev</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="text-align: left;"><b>Placebo</b></td>
            <td style="text-align: center;">1.5</td>
            <td style="text-align: center;">42</td>
            <td style="text-align: center;">2.6</td>
        </tr> 
        <tr>
            <td style="text-align: left;"><b>Dosage 1</b></td>
            <td style="text-align: center;">2.3</td>
            <td style="text-align: center;">41</td>
            <td style="text-align: center;">2.6</td>
        </tr>  
        <tr>
            <td style="text-align: left;"><b>Dosage 2</b></td>
            <td style="text-align: center;">3.5</td>
            <td style="text-align: center;">43</td>
            <td style="text-align: center;">3.3</td>
        </tr>  
        <tr>
            <td style="text-align: left;"><b>Dosage 3</b></td>
            <td style="text-align: center;">6.8</td>
            <td style="text-align: center;">44</td>
            <td style="text-align: center;">7.3</td>
        </tr>   
        <tr>
            <td style="text-align: left;"></td>
            <td style="text-align: center;"></td>
            <td style="text-align: center;"></td>
            <td style="text-align: center;"></td>
        </tr>   
        <tr style="background-color: #EEEEEE;">
            <td style="text-align: left;   background-color: #EEEEEE;"><b>Dosage 1+2+3</b></td>
            <td style="text-align: center; background-color: #EEEEEE;">4.3</td>
            <td style="text-align: center; background-color: #EEEEEE;">128</td>
            <td style="text-align: center; background-color: #EEEEEE;">5.2</td>
        </tr>                                     
    </tbody>
</table>

Based upon the following math: 

<table>
    <thead>
        <tr>
            <th style="text-align: left;">Data</th>
            <th style="text-align: center;">Mean</th>
            <th style="text-align: center;">Population</th>
            <th style="text-align: center;">Std Dev</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="text-align: left;"><b>Dosage 1</b></td>
            <td style="text-align: center;">2.3</td>
            <td style="text-align: center;">41</td>
            <td style="text-align: center;">2.6</td>
        </tr>  
        <tr>
            <td style="text-align: left;"><b>Dosage 2</b></td>
            <td style="text-align: center;">3.5</td>
            <td style="text-align: center;">43</td>
            <td style="text-align: center;">3.3</td>
        </tr>  
        <tr style="background-color: #EEEEEE;">
            <td style="text-align: left;   background-color: #EEEEEE;"><b>Dosage 1+2</b></td>
            <td style="text-align: center; background-color: #EEEEEE;">2.9</td>
            <td style="text-align: center; background-color: #EEEEEE;">84</td>
            <td style="text-align: center; background-color: #EEEEEE;">3.0</td>
        </tr> 
        <tr>
            <td style="text-align: left;"></td>
            <td style="text-align: center;"></td>
            <td style="text-align: center;"></td>
            <td style="text-align: center;"></td>
        </tr>
        <tr>
            <td style="text-align: left;"><b>Dosage 1+2</b></td>
            <td style="text-align: center;">2.9</td>
            <td style="text-align: center;">84</td>
            <td style="text-align: center;">3.0</td>
        </tr>
        <tr>
            <td style="text-align: left;"><b>Dosage 3</b></td>
            <td style="text-align: center;">6.8</td>
            <td style="text-align: center;">44</td>
            <td style="text-align: center;">7.3</td>
        </tr>                                      
        <tr style="background-color: #EEEEEE;">
            <td style="text-align: left;   background-color: #EEEEEE;"><b>Dosage 1+2+3</b></td>
            <td style="text-align: center; background-color: #EEEEEE;">4.3</td>
            <td style="text-align: center; background-color: #EEEEEE;">128</td>
            <td style="text-align: center; background-color: #EEEEEE;">5.2</td>
        </tr>                                     
    </tbody>
</table>


Given the above, we can see that Dosage 1 and Dosage 2 are merged together [as follows](https://handbook-5-1.cochrane.org/chapter_7/table_7_7_a_formulae_for_combining_groups.htm):

* **Mean:**  Calculate the weighted average of the given dosages ((Mean 1 * Pop 1) + (Mean 2 * Pop 2)) / (Pop 1 + Pop 2)

* **Population:**  Add the populations together (Pop1 + Pop2)

* **Standard Deviation:**  

{% include image.html name="standard_deviation_calculation.gif" alt="Standard Deviation Calculation" class="header-image" %} 
 
Given the length of the standard deviation calculation - it is preferable to combine more than two studies by simply combining the first two studies together, and then combine this result with the third study, and then combine the following result with the fourth study, and so on.  An example of this approach has been demonstrated above. 
