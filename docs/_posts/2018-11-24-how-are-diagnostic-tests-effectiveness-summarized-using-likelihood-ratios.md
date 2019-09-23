---
layout: post
title: How Are Diagnostic Tests' Effectiveness Summarized Using Likelihood Ratios?   
description: An overview of likelihood ratios and how they might be interpreted to determine the significance of an intervention
tags: Diagnostic_Tests Likelihood_Ratio
---

{% include image.html name="header_22_resized.jpg" alt="How Are Diagnostic Tests' Effectiveness Summarized Using Likelihood Ratios" class="header-image" %} 

<p style="color: grey"><i>An overview of likelihood ratios and how they might be interpreted to determine the significance of an intervention</i></p>


<!--more-->

As previously established, we can calculate Positive and Negative Likelihood Ratios as follows:

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
            <td style="text-align: left;"><b>Positive Likelihood Ratio</b></td>
            <td style="text-align: left;">Sensitivity / (1 - Specificity)</td>
            <td style="text-align: left;">How much more likely a patient with the target disease will receive a positive test result compared to patients without the disease</td>
        </tr>
        <tr>
            <td style="text-align: left;"><b>Negative Likelihood Ratio</b></td>
            <td style="text-align: left;">(1 - Sensitivity) / Specificity</td>
            <td style="text-align: left;">How much more likely a patient with the target disease will receive a negative test result compared to patients without the disease</td>  
        </tr>                                                        
    </tbody>
</table>

As Likelihood Ratios combine both Sensitivity (correctly rule-in disease) and Specificity (correctly rule-out disease) they provide a [good overarching view](http://getthediagnosis.org/definitions.html) of a particular diagnostic test.   For example, when we calculate a Positive Likelihood Ratio of 15, [this means](https://canadiem.org/how-to-use-likelihood-ratios/) we have 15 true positive test results for every 1 false positive - which is rather robust.  Turning to the Negative Likelihood Ratio, a calculated value of 0.1 has 1 false negative for every 10 true negatives (or 1/10) - which is also fairly encouraging. 

Furthermore, a Likelihood Ratio [can also be correlated](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC1495095/) with a specific increased probability (Positive Likelihood Ratio) or decreased probability (Negative Likelihood Ratio) that a patient has a target disease.  These probabilities can then be used to get a [qualitative](https://www.uws.edu/wp-content/uploads/2013/10/Likelihood_Ratios.pdf) [interpretation](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=5&cad=rja&uact=8&ved=0ahUKEwjk2carz-TZAhVsneAKHdsNCgcQFghfMAQ&url=https%3A%2F%2Fmclibrary.duke.edu%2Fsites%2Fmclibrary.duke.edu%2Ffiles%2Fpublic%2Fguides%2Flikelihood-ratios.doc&usg=AOvVaw3wFEzbq8cRwDovXma2Vm1R) [of](https://www.med.emory.edu/EMAC/curriculum/diagnosis/lr%27s.htm) [the](http://medtrain.chm.msu.edu/ebm/Diagnosis/Diagnosis6.html) [diagnostic](http://www.ptolemy.ca/members/ebm/Jaeschke19942.pdf) test's overall significance as a general 'rule of thumb':

**Positive Likelihood Ratio:**

<table>
    <thead>
        <tr>
            <th style="text-align: left;">Value</th>
            <th style="text-align: left;">Change In Probability</th>
            <th style="text-align: left;">Qualitative Significance</th>                 
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="text-align: left;">11.00</td>
            <td style="text-align: left;"></td>
            <td style="text-align: left;">Large</td>
        </tr>
        <tr>
            <td style="text-align: left;">10.00</td>
            <td style="text-align: left;">45%</td>
            <td style="text-align: left;">Medium</td>
        </tr>
        <tr>
            <td style="text-align: left;">9.00</td>
            <td style="text-align: left;">43%</td>
            <td style="text-align: left;">Medium</td>
        </tr>
        <tr>
            <td style="text-align: left;">8.00</td>
            <td style="text-align: left;">40%</td>
            <td style="text-align: left;">Medium</td>
        </tr>
        <tr>
            <td style="text-align: left;">7.00</td>
            <td style="text-align: left;">38%</td>
            <td style="text-align: left;">Medium</td>
        </tr>
        <tr>
            <td style="text-align: left;">6.00</td>
            <td style="text-align: left;">35%</td>
            <td style="text-align: left;">Medium</td>
        </tr>
        <tr>
            <td style="text-align: left;">5.00</td>
            <td style="text-align: left;">30%</td>
            <td style="text-align: left;">Medium</td>
        </tr>
        <tr>
            <td style="text-align: left;">4.00</td>
            <td style="text-align: left;">25%</td>
            <td style="text-align: left;">Small</td>
        </tr>
        <tr>
            <td style="text-align: left;">3.00</td>
            <td style="text-align: left;">20%</td>
            <td style="text-align: left;">Small</td>
        </tr>   
        <tr>
            <td style="text-align: left;">2.00</td>
            <td style="text-align: left;">15%</td>
            <td style="text-align: left;">Small</td>
        </tr> 
        <tr>
            <td style="text-align: left;">1.00</td>
            <td style="text-align: left;">8%</td>
            <td style="text-align: left;">None</td>
        </tr>
        <tr>
            <td style="text-align: left;">0.00</td>
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
            <th style="text-align: left;">Change In Probability</th>
            <th style="text-align: left;">Qualitative Significance</th>                 
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="text-align: left;">0.00</td>
            <td style="text-align: left;">0%</td>
            <td style="text-align: left;">None</td>
        </tr>
        <tr>
            <td style="text-align: left;">0.05</td>
            <td style="text-align: left;"></td>
            <td style="text-align: left;">Large</td>
        </tr>
        <tr>
            <td style="text-align: left;">0.10</td>
            <td style="text-align: left;">-45%</td>
            <td style="text-align: left;">Medium</td>
        </tr>
        <tr>
            <td style="text-align: left;">0.15</td>
            <td style="text-align: left;"></td>
            <td style="text-align: left;">Medium</td>
        </tr>
        <tr>
            <td style="text-align: left;">0.20</td>
            <td style="text-align: left;">-30%</td>
            <td style="text-align: left;">Medium</td>
        </tr>
        <tr>
            <td style="text-align: left;">0.25</td>
            <td style="text-align: left;"></td>
            <td style="text-align: left;">Small</td>
        </tr>
        <tr>
            <td style="text-align: left;">0.30</td>
            <td style="text-align: left;">-25%</td>
            <td style="text-align: left;">Small</td>
        </tr>
        <tr>
            <td style="text-align: left;">0.35</td>
            <td style="text-align: left;"></td>
            <td style="text-align: left;">Small</td>
        </tr>
        <tr>
            <td style="text-align: left;">0.40</td>
            <td style="text-align: left;">-20%</td>
            <td style="text-align: left;">Small</td>
        </tr>   
        <tr>
            <td style="text-align: left;">0.45</td>
            <td style="text-align: left;"></td>
            <td style="text-align: left;">Small</td>
        </tr> 
        <tr>
            <td style="text-align: left;">0.50</td>
            <td style="text-align: left;">-15%</td>
            <td style="text-align: left;">Small</td>
        </tr>                                                                                                                              
    </tbody>
</table>

Based on the above chart, a diagnostic test can be evaluated as follows:

* **Positive Likelihood Ratio:**  The higher the likelihood ratio, the more likely the diagnostic test rules-in a disease (i.e.; test has a high true positive); this ratio requires a high Specificity

* **Negative Likelihood Ratio:**  The lower the likelihood ratio , the more likely the diagnostic test rules-out a disease (i.e.; test has a low false negative); this ratio requires a high Sensitivity.

While rare, a [good](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4975285/) ([conclusive](https://books.google.com/books?id=9c9omEvDV7IC&pg=PA21&lpg=PA21&dq=diagnostic+likelihood+ratio+1+2+5+10&source=bl&ots=SS3v4AZC1d&sig=sUXNJzaghYUS531irpOJ-1kfMIg&hl=en&sa=X&ved=0ahUKEwims-D61-TZAhXMmVkKHUMgDOU4ChDoAQg7MAY#v=onepage&q=diagnostic%20likelihood%20ratio%201%202%205%2010&f=false)) diagnostic test will have likelihood ratios that can be interpreted as having "large" qualitative significance - in other words the test delivers high true positives and low false negatives.  To arrive at this level of confidence, a diagnostic test's Sensitivity and Specificity will both typically need to exceed 90% (with potential for some give-and-take between the two values).   




