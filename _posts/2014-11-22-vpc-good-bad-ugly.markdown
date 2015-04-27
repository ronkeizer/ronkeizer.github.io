---
layout: post
title:  "Visual predictive checks: 'the good, the bad, and the ugly'"
date:   2014-11-22 12:00:34
categories: nonmem update
---

The VPC is the most commonly used diagnostic in pharmacometrics. That is not just my opinion, I also collected a bit of evidence: on a recent big pharmacometrics meeting (ACoP 2014) I noticed that about 90% of all posters that included model evaluation used a VPC to show model performance. The remainder 10% used either only standard GOF plots, while 1 poster showed prediction discrepancies (PDE, not NPDE).

While the VPC is clearly the most widely used diagnostic on this side of the Atlantic, there is a huge variety in how these plots are displayed and what (dis-)information they show. The VPC easily has five fairly different versions that are all quite commonly presented. However, I feel that if it comes to usefulness and power, some versions should be counted as more equal than others...

## What is the purpose of the VPC?
In my view, the purpose is to see if the model can predict, for the exact same design as the model, the longitudinal (or an independent variable other than time) trend of the observed data as well as its variability for the population. 

So __error 1__ in my view is when  

## What should the VPC show?
Let me start with some examples of what I think are 'VPC' that are not showing the right information.

## What should the VPC show?


## Binning
In my opinion, a fully automated approach has both advantages as disadvantages. The advantages are obvious: it is user-independent, it is easier, binning can be pre-specified in analysis plans, etc. However, it also has an important drawback, as it withholds users from actually looking at the data and thinking about the bin placement themselves. This becomes more important when there are no or few very spread-out clusters in the data, which can e.g. occur with routinely collected clinical data. For such cases, I am not convinced that the automated approaches will always select more optimal binning approaches than manual binning, and I actually would like to have more control. At this point I don't have a clear-cut example of where manual binning worked better, but I will post it here if I encounter one. 

## The ugly
Finally, besides showing the right information, don't forget that it would be nice if the plots are aesthetically appealing. Please keep in mind that nobody wants to look at plots with bright green or purple colors (also read [this](http://www.edwardtufte.com/bboard/q-and-a-fetch-msg?msg_id=0000HT)), and please don't overlay 12,000 datapoints over your prediction intervals... 
