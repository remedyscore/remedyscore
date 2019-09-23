---
layout: post
title: How Can We Combine Studies With Different Methodologies?   
description: An overview of using forest plots, interaction tests, random effects model, and other techniques to combine studies with different underlying methodologies 
tags: Effect_Sizes I-Squared Random_Effects_Model
---

{% include image.html name="header_18_2_resized.jpg" alt="How Can We Combine Studies With Different Methodologies" class="header-image" %} 

<p style="color: grey"><i>An overview of using forest plots, interaction tests, random effects model, and other techniques to combine studies with different underlying methodologies</i></p>


<!--more-->

Effect sizes measure the size and direction of an outcome.  For example, the Standardized Mean Difference indicates the size of an effect compared to the standard deviation of a sampled population.  Effect sizes do not speak towards the statistical significance of the effect.  A large Standardized Mean Difference doesn't necessarily mean that an effect actually exists.

In fact, when attempting to combine together multiple effect sizes for use in a meta-analysis, it is possible that the individual effect sizes were all calculated from studies using very different methodologies.  For this reason, there needs to be a check that the effects found in the individual studies are similar enough that one can be confident that a combined estimate will be a meaningful description of the underlying set of studies.
 
Heterogeneity, or how the degree to which effect sizes are dispersed around a central mean, can be tested for visually and quantitatively:
  
* **Forest-Plot Graphs:**  Visually plot the effect sizes of studies as boxes or diamonds and denote the confidence intervals with a line that extends to the left and right of the effect size.  When the confidence intervals of these studies have poor overlap, it is a visual sign of heterogeneity. 

* **Interaction Test (Multiple Studies):**  We calculate I^2 to help determine if the variation in the studies is statistically relevant (and not just random noise / sampling error) and the degree the variation exist. Visually, I^2 is the degree effect sizes are dispersed around a central mean.
 
    The Interaction Test is calculated as ( Q – df / Q ) x 100%, where:

    * **Q / Chi-Squared Statistic:**  This represents the chi-squared statistic, which can be calculated as (Effect Size^2 * Weight) – ( (Effect Size * Weight) / Weight) )

    * **df:**  This represents the degrees of freedom, or the number of studies minus one.

    * **p-value:**  The p-value of a given Q or chi-squared statistic can be calculated by using CHIDIST(Q, df – 1).  Typically, a p-value below 10% is an indicator of statistical significance, and a value above this threshold indicates heterogeneity in results. 

    For example, using the Fixed Effects Model, we see this calculation in action below: 
    
    <table>
        <thead>
            <tr>
                <th style="text-align: left;">Study</th>
                <th style="text-align: left;">Effect Size (E)</th>
                <th style="text-align: left;">Variance Within (V)</th>
                <th style="text-align: left;">Weight (W) or (1/V)</th>  
                <th style="text-align: left;">E x W</th>  
                <th style="text-align: left;">E^2 x W</th>                          
                <th style="text-align: left;">W^2</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td style="text-align: left;"><b>Study 1</b></td>
                <td style="text-align: left;">0.11</td>
                <td style="text-align: left;">0.01</td>
                <td style="text-align: left;">100</td>
                <td style="text-align: left;">11</td>
                <td style="text-align: left;">1.21</td>            
                <td style="text-align: left;">10,000.00</td>
            </tr>
            <tr>
                <td style="text-align: left;"><b>Study 2</b></td>
                <td style="text-align: left;">0.22</td>
                <td style="text-align: left;">0.03</td>
                <td style="text-align: left;">33.33</td>
                <td style="text-align: left;">7.47</td>
                <td style="text-align: left;">1.67</td>            
                <td style="text-align: left;">1,111.11</td>
            </tr> 
            <tr>
                <td style="text-align: left;"><b>Study 3</b></td>
                <td style="text-align: left;">0.34</td>
                <td style="text-align: left;">0.02</td>
                <td style="text-align: left;">50</td>
                <td style="text-align: left;">16.88</td>
                <td style="text-align: left;">5.7</td>            
                <td style="text-align: left;">2,500.00</td>
            </tr>       
            <tr>
                <td style="text-align: left;"><b>Study 4</b></td>
                <td style="text-align: left;">0.45</td>
                <td style="text-align: left;">0.02</td>
                <td style="text-align: left;">66.67</td>
                <td style="text-align: left;">30.06</td>
                <td style="text-align: left;">13.56</td>            
                <td style="text-align: left;">4,444.44</td>
            </tr>
            <tr>
                <td style="text-align: left;"><b>Study 5</b></td>
                <td style="text-align: left;">0.48</td>
                <td style="text-align: left;">0.01</td>
                <td style="text-align: left;">100</td>
                <td style="text-align: left;">48</td>
                <td style="text-align: left;">23.04</td>            
                <td style="text-align: left;">10,000.00</td>
            </tr> 
            <tr>
                <td style="text-align: left; background-color: #EEEEEE;"><b>Total</b></td>
                <td style="text-align: left; background-color: #EEEEEE;"><b>1.60</b></td>
                <td style="text-align: left; background-color: #EEEEEE;"><b>0.09</b></td>
                <td style="text-align: left; background-color: #EEEEEE;"><b>350</b></td>
                <td style="text-align: left; background-color: #EEEEEE;"><b>113.41</b></td>
                <td style="text-align: left; background-color: #EEEEEE;"><b>45.18</b></td>            
                <td style="text-align: left; background-color: #EEEEEE;"><b>28,055.56</b></td>
            </tr>                                                                                        
        </tbody>
    </table>
    
    <table>
        <thead>
            <tr>
                <th style="text-align: left;">Variable</th>
                <th style="text-align: left;">Value</th>
                <th style="text-align: left;">Calculation</th> 
            </tr>
        </thead>
        <tbody>
            <tr>
                <td style="text-align: left;"><b>Q</b></td>
                <td style="text-align: left;">8.43</td>
                <td style="text-align: left;">=E^2W-(EW^2/W)</td>                
            </tr>
            <tr>
                <td style="text-align: left;"><b>df</b></td>
                <td style="text-align: left;">4</td>
                <td style="text-align: left;">=Studies - 1</td>
            </tr> 
            <tr>
                <td style="text-align: left;"><b>p-value</b></td>
                <td style="text-align: left;">0.08</td>
                <td style="text-align: left;">=CHIDIST(Q, df)</td>                
            </tr>       
            <tr>
                <td style="text-align: left;"><b>I-Squared</b></td>
                <td style="text-align: left;">0.53</td>
                <td style="text-align: left;">=((Q - df)/Q) * 100%</td>                
            </tr>
        </tbody>
    </table>    
    
    <table>
        <thead>
            <tr>
                <th style="text-align: left;">Variable</th>
                <th style="text-align: left;">Value</th>
                <th style="text-align: left;">Calculation</th> 
            </tr>
        </thead>
        <tbody>
            <tr>
                <td style="text-align: left;"><b>Numerator</b></td>
                <td style="text-align: left;">4.43</td>
                <td style="text-align: left;">=MAX(Q-df, 0)</td>                
            </tr>
            <tr>
                <td style="text-align: left;"><b>C</b></td>
                <td style="text-align: left;">269.84</td>
                <td style="text-align: left;">=W-(W^2/W)</td>
            </tr> 
            <tr>
                <td style="text-align: left;"><b>Tau-Squared</b></td>
                <td style="text-align: left;">0.02</td>
                <td style="text-align: left;">=Numerator/C</td>                
            </tr>       
        </tbody>
    </table>

    * After I^2 has been derived, it can be interpreted as follows:
    
    <table>
        <thead>
            <tr>
                <th style="text-align: left;">Interaction %</th>
                <th style="text-align: left;">Heterogeneity</th>                 
            </tr>
        </thead>
        <tbody>
            <tr>
                <td style="text-align: left;"><b>Interaction < 00%</b></td>
                <td style="text-align: left;">No Heterogeneity</td>
            </tr>
            <tr>
                <td style="text-align: left;"><b>Interaction < 40%</b></td>
                <td style="text-align: left;">Low Heterogeneity</td>
            </tr> 
            <tr>
                <td style="text-align: left;"><b>Interaction < 60%</b></td>
                <td style="text-align: left;">Moderate Heterogeneity</td>
            </tr>   
            <tr>
                <td style="text-align: left;"><b>Interaction > 60%</b></td>
                <td style="text-align: left;">High Heterogeneity</td>
            </tr>                    
        </tbody>
    </table>

*  **Interaction Test (Single Study):**  We can also calculate I^2 in a similar manner as above for single studies:
 
    * **Q / Chi-Squared Statistic:**  This represents the chi-squared statistic, which can be calculated as follows:
    
    <table>
        <thead>
            <tr>
                <th style="text-align: left;">Group</th>
                <th style="text-align: left;">Pass</th>
                <th style="text-align: left;">Fail</th>
                <th style="text-align: left;">Total</th>                 
            </tr>
        </thead>
        <tbody>
            <tr>
                <td style="text-align: left;"><b>Group A</b></td>
                <td style="text-align: center;">36</td>
                <td style="text-align: center;">14</td>
                <td style="text-align: center; background-color: #EEEEEE;">50</td>
            </tr>
            <tr>
                <td style="text-align: left;"><b>Group B</b></td>
                <td style="text-align: center;">30</td>
                <td style="text-align: center;">25</td>
                <td style="text-align: center; background-color: #EEEEEE;">55</td>
            </tr> 
            <tr>
                <td style="text-align: left;  background-color: #EEEEEE;"><b>Total</b></td>
                <td style="text-align: center; background-color: #EEEEEE;"><b>66</b></td>
                <td style="text-align: center; background-color: #EEEEEE;"><b>39</b></td>
                <td style="text-align: center; background-color: #EEEEEE;"><b>105</b></td>
            </tr>   
        </tbody>
    </table>
        	 	 	 	 	 
    * **Q Value:** 3.417673236	 ( 105*((36*25)-(14*30))^2 / (50*55*66*39) )
    
    * **df:** This represents the degrees of freedom, or typically the number of observations minus one.  For example, in a simple review of an intervention group and control group, the degrees of freedom are one (2 – 1 = 1).   For more complicated observations, that may have subgroups, degrees of freedom are typically calculated as (rows – 1) x (columns – 1).  For example, Group A, Group B, and Group C (columns) and Male and Female (rows), you would result in (2 – 1) * (3 – 1) = 2 degrees of freedom.
    
    * **p-value:** The p-value is calculated in the same manner as above, using CHIDIST(Q, df – 1).	 

However, the I^2 metric can sometimes be [misleading](https://www.meta-analysis-workshops.com/download/common-mistakes1.pdf) - as determining heterogeneity often requires specific context about the meta-analysis being conducted.  To that end, rather than simply test to see if heterogeneity exists - and then do something to fix it - it is better to [assume](https://www.meta-analysis-workshops.com/download/common-mistakes2.pdf) [it exists](https://academic.oup.com/ije/article/37/5/1158/871288) and employ a solution.

There are a few options for managing the likely appearance of statistical heterogeneity in a meta-analysis:
 
* **Uses Random Effects Model:**  One analytical approach to heterogeneity is to incorporate it into a [random](http://www.wvbauer.com/lib/exe/fetch.php/articles:viechtbauer2007c.pdf) [effects](https://www.meta-analysis-workshops.com/download/common-mistakes2.pdf) model. A random effects model involves an assumption that the effects being estimated in the different studies are not identical, but follow some distribution. The model represents the lack of knowledge about why real, or apparent, treatment effects differ by treating the differences as if they were random. 

* **Split Studies:**  It may not be appropriate to combine all existing studies within the given meta-analysis.  Instead, it could be advisable to split studies into less heterogeneous groups based on their study characteristics and the location of the studies on a forest plot.
