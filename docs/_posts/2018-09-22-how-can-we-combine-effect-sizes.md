---
layout: post
title: How Can We Combine Effect Sizes?   
description: An overview of combining studies using a fixed and random effects model 
tags: Effect_Sizes Fixed_Effects_Model Random_Effects_Model
---

{% include image.html name="header_16_resized.jpg" alt="How Can We Combine Effect Sizes" class="header-image" %} 

<p style="color: grey"><i>An overview of combining studies using a fixed and random effects model</i></p>


<!--more-->

Once Effect Sizes have been calculated for a series of studies, they can be combined using [one of two methods](https://www.meta-analysis.com/downloads/Meta-analysis%20Fixed-effect%20vs%20Random-effects%20models.pdf): 

* **Fixed Effects Model / Inverse Variance:**  Assumes all studies in the meta-analysis draw from a common population, which means we can assign weights to the studies based entirely on the study's individual Effect Size.  A large study would be given the lion's share of the weight, and a small study could be largely ignored.   This method of combining Effect Sizes is sometimes called "inverse variance", the weight of each study is the inverse of its variance.  

  Mathematically, this might be calculated as follows:
  
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

  We then derive an Effect Size as (Total Effect Size x Weight) / Total Weight or 113.41 / 350

* **Random Effects Model:**  The random effects model assumes that the studies were drawn from populations that differ from each other in ways that could have an impact on the treatment's effect. When a researcher is accumulating data from a series of studies that had been performed by other people, it would be very unlikely that all the studies were functionally equivalent.  Almost invariably, the subjects or interventions in these studies would differ in ways that impact the results, and therefore we should not assume a common Effect Size.
   
  To account for differences in studies, this requires that we mathematically [calculate](https://www.meta-analysis.com/downloads/M-a_f_e_v_r_e_sv.pdf) (a) the variance within a study and (b) the variance between studies, and sum these two values and take their inverse to derive a weighting for each study.  This is exactly the same process as for the Fixed Effects Model – but includes the notion of calculating the variance between studies, sometimes called "tau-squared" or "τ^2".

  Tau-Squared is calculated using three component parts: 

  * **Q / Chi-Squared Statistic (E^2W-(EW^2/W):**  The total variance of the studies

  * **df / Degrees of Freedom (Studies – 1):**  Number of values that are free to vary in our analysis (one value will always remain fixed)

  * **C (W-(W^2/W)):**  A scaling factor to ensure that variance between studies uses the same metric as the variance within studies

  With these component parts, we can derive tau-squared as: MAX(Q-df, 0) / C, and use this value as a constant within our Random Effects Model calculations.
  
    <table>
        <thead>
            <tr>
                <th style="text-align: left;">Study</th>
                <th style="text-align: left;">Effect Size (E)</th>
                <th style="text-align: left;">Variance Within (V)</th>
                <th style="text-align: left;">Variance Between (Tau-Squared)</th>  
                <th style="text-align: left;">Variance Total (V+Tau)</th>  
                <th style="text-align: left;">Weight (W) (1/V)</th>
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
                <td style="text-align: left;">0.02</td>
                <td style="text-align: left;">0.03</td>
                <td style="text-align: left;">37.86</td>            
                <td style="text-align: left;">4.16</td>
                <td style="text-align: left;">0.46</td>
                <td style="text-align: left;">1,433.25</td>                
            </tr>
            <tr>
                <td style="text-align: left;"><b>Study 2</b></td>
                <td style="text-align: left;">0.22</td>
                <td style="text-align: left;">0.03</td>
                <td style="text-align: left;">0.02</td>
                <td style="text-align: left;">0.05</td>
                <td style="text-align: left;">21.55</td>            
                <td style="text-align: left;">4.83</td>
                <td style="text-align: left;">1.08</td>
                <td style="text-align: left;">464.19</td>                 
            </tr> 
            <tr>
                <td style="text-align: left;"><b>Study 3</b></td>
                <td style="text-align: left;">0.34</td>
                <td style="text-align: left;">0.02</td>
                <td style="text-align: left;">0.02</td>
                <td style="text-align: left;">0.04</td>
                <td style="text-align: left;">27.46</td>            
                <td style="text-align: left;">9.27</td>
                <td style="text-align: left;">3.13</td>
                <td style="text-align: left;">754.15</td>                 
            </tr>       
            <tr>
                <td style="text-align: left;"><b>Study 4</b></td>
                <td style="text-align: left;">0.45</td>
                <td style="text-align: left;">0.02</td>
                <td style="text-align: left;">0.02</td>
                <td style="text-align: left;">0.03</td>
                <td style="text-align: left;">31.83</td>            
                <td style="text-align: left;">14.36</td>
                <td style="text-align: left;">6.47</td>
                <td style="text-align: left;">1,013.32</td>                 
            </tr>
            <tr>
                <td style="text-align: left;"><b>Study 5</b></td>
                <td style="text-align: left;">0.48</td>
                <td style="text-align: left;">0.01</td>
                <td style="text-align: left;">0.02</td>
                <td style="text-align: left;">0.03</td>
                <td style="text-align: left;">37.86</td>            
                <td style="text-align: left;">18.17</td>
                <td style="text-align: left;">8.72</td>
                <td style="text-align: left;">1,433.25</td>                 
            </tr> 
            <tr>
                <td style="text-align: left; background-color: #EEEEEE;"><b>Total</b></td>
                <td style="text-align: left; background-color: #EEEEEE;"><b>1.60</b></td>
                <td style="text-align: left; background-color: #EEEEEE;"><b>0.09</b></td>
                <td style="text-align: left; background-color: #EEEEEE;"><b>0.08</b></td>
                <td style="text-align: left; background-color: #EEEEEE;"><b>0.17</b></td>
                <td style="text-align: left; background-color: #EEEEEE;"><b>156.56</b></td>            
                <td style="text-align: left; background-color: #EEEEEE;"><b>50.79</b></td>
                <td style="text-align: left; background-color: #EEEEEE;"><b>19.87</b></td>            
                <td style="text-align: left; background-color: #EEEEEE;"><b>5,098.16</b></td>                
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
                <td style="text-align: left;">3.39</td>
                <td style="text-align: left;">=E^2W-(EW^2/W)</td>                
            </tr>
            <tr>
                <td style="text-align: left;"><b>df</b></td>
                <td style="text-align: left;">4</td>
                <td style="text-align: left;">=Studies - 1</td>
            </tr> 
            <tr>
                <td style="text-align: left;"><b>p-value</b></td>
                <td style="text-align: left;">0.5</td>
                <td style="text-align: left;">=CHIDIST(Q, df)</td>                
            </tr>       
            <tr>
                <td style="text-align: left;"><b>I-Squared</b></td>
                <td style="text-align: left;">-0.18</td>
                <td style="text-align: left;">=((Q - df)/Q) * 100%</td>                
            </tr>
        </tbody>
    </table>    

  We then derive an Effect Sized as (Total Effect Size x Weight) / Total Weight or 50.79 / 156.56.

In summary of the above, it is usually preferable to combine together Effect Sizes using the Random Effects Model, as it helps account for variance between studies.  This helps mitigate potential differences in studies and avoids overstating an Effect Size. 
