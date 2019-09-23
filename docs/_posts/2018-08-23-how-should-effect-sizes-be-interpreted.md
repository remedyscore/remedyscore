---
layout: post
title: How Should Effect Sizes Be Interpreted?   
description: An overview of interpreting effect sizes for continuous and dichotomous data 
tags: Effect_Sizes Dichotomous_Data Continuous_Data 
---

{% include image.html name="header_13_resized.jpg" alt="How Should Effect Sizes Be Interpreted" class="header-image" %} 

<p style="color: grey"><i>An overview of interpreting effect sizes for continuous and dichotomous data</i></p>


<!--more-->

After calculating an Effect Size for Continuous or Dichotomous Data, it can be helpful to have general rules of thumb to interpret the magnitude of a given result. 

## CONTINUOUS DATA:

For Continuous Data, the following [scale](https://www.psychometrica.de/effect_size.html#cohen) can be helpful for interpreting Effect Sizes calculated with a Pooled Standard Deviation containing Cohen's d (or [Hedge's g](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2848393/) for that matter): 

<table>
    <thead>
        <tr>
            <th style="text-align: left;">Data Type</th>
            <th style="text-align: center;">Adverse Effect</th>
            <th style="text-align: center;">No Effect</th>
            <th style="text-align: center;">Small Effect</th>
            <th style="text-align: center;">Medium Effect</th>
            <th style="text-align: center;">Large Effect</th>            
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="text-align: left;"><b>Continuous Data</b></td>
            <td style="text-align: center;">< 0.00</td>
            <td style="text-align: center;">0.00 - 0.01</td>
            <td style="text-align: center;">0.20 - 0.40</td>
            <td style="text-align: center;">0.50 - 0.70</td>
            <td style="text-align: center;">> 0.80</td>
        </tr>                     
    </tbody>
</table>

As the Standard Mean Difference effectively measures standard deviations between the treatment and control group, it can also be helpful to [visualize](http://rpsychologist.com/d3/cohend/) or describe this value using [Cohen's U3](https://figuraleffect.wordpress.com/2013/11/20/cohens-u1-u2-and-u3/); for example a Cohen's D of 0.3 also implies that 62% of the treatment group will be above the mean of the control group. 

## DICHOTOMOUS DATA:

For Dichotomous Data, there are various methodologies for interpreting Odds Ratios in a manner consistent with Cohen's d / Hedge's g at 0.2 (small), 0.5 (medium), and 0.8 (large), including: 

* 1.2 (small), 1.9 (medium), and 3.0 (large) :: [Source](http://journals.plos.org/plosone/article?id=10.1371/journal.pone.0058777) (aggressive for large effect)

* 1.5 (small), 2.5 (medium), and 4.3 (large) :: [Source](https://www.scribd.com/presentation/135169182/8-Interpretation) / [Source](http://www.google.co.uk/url?sa=t&rct=j&q=&esrc=s&source=web&cd=3&ved=0CEQQFjAC&url=http%3A%2F%2Fpsych.unl.edu%2Fpsycrs%2F971%2Fmeta%2Feffect_sizes.ppt&ei=qlWHVJvADoT4UNv_gCA&usg=AFQjCNHG3CSxFRIOCIsjPcZTDMIHLpytdQ&bvm=bv.81449611,d.d24) / [Source](http://mason.gmu.edu/~dwilsonb/downloads/interpretation.ppt)

* 1.7 (small), 3.5 (medium), and 6.7 (large) :: [Source](http://www.tandfonline.com/doi/abs/10.1080/03610911003650383)

* 2.0 (small), 3.0 (medium), and 4.0 (large) :: [Source](http://psychology.okstate.edu/faculty/jgrice/psyc5314/AnEffectSizePrimer_2009.pdf) [(aggressive for large effect)](http://journals.plos.org/plosone/article?id=10.1371/journal.pone.0058777)

* 1.5 (small), 3.5 (medium), and 9.0 (large) :: [Source](http://imaging.mrc-cbu.cam.ac.uk/statswiki/FAQ/effectSize) 

In general, then, we could [summarize the above as](http://www.biometrics.org.au/conferences/Hobart2015/talks2015/Monday/C_0940_Mon_JakeOliver.pdf):

* **Minimum:**   1.2 (small), 1.9 (medium), and 3.0 (large)

* **Average:**  1.3 (small), 2.4 (medium, and 4.7 (large)

* **Maximum:**  2.0 (small), 3.5 (medium), and 9.0 (large)

Therefore - in the spirit of being conservative and also [mirroring](http://imaging.mrc-cbu.cam.ac.uk/statswiki/FAQ/effectSize) Cohen's direct equivalency – we might use a rule of thumb indicating 2.0 (small), 3.5 (medium), 9.0 (large); which is effectively the maximum end of the above range.  This would mean: 

<table>
    <thead>
        <tr>
            <th style="text-align: left;">Data Type</th>
            <th style="text-align: center;">Adverse Effect</th>
            <th style="text-align: center;">No Effect</th>
            <th style="text-align: center;">Small Effect</th>
            <th style="text-align: center;">Medium Effect</th>
            <th style="text-align: center;">Large Effect</th>            
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="text-align: left;"><b>Dichotomous Data</b></td>
            <td style="text-align: center;">< 0.00</td>
            <td style="text-align: center;">0.00 - 2.00</td>
            <td style="text-align: center;">2.00 - 3.00</td>
            <td style="text-align: center;">3.00 - 9.00</td>
            <td style="text-align: center;">> 9.00</td>
        </tr>                     
    </tbody>
</table>
