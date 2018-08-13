# A Measurement Study on Multi-path TCP with Multiple Cellular Carriers on High Speed Rails
* [Li Li] 
* [Keywords: Multi-path TCP, Measurement, Cellular Networks, High Speed Rails]

## Abstract

> ### 1. Motivation
> The performance of traditional single-path transmission degrades significantly during high speed mobility due to frequent handoff.
> 
> Multi-path transmission with multiple carriers is a promising way to enhance
the performance. 
> 
> ### 2.Contriution
> First we measure `Multi-Path TCP (MPTCP)` with two cellular carriers on HSRs with a peak speed of 310km/h.  And find a significant difference in handoff time between two carriers.
> 
> > * [Advantage]:
> >  
> > MPTCP can provide much better performance than TCP in the poorer of the two paths. This indicates that MPTCP’s robustness to handoff is much
higher than TCP’s.
> 
> > * [Disadvantage]:
> > 
> > MPTCP performs worse than TCP in the better path most of the time .
> > We find that the low efficiency can be attributed to poor adaptability to frequent handoff by MPTCP’s key operations in sub-flow establishment, congestion control and scheduling.
---

## Introduction

>### Present Situation:

> There is a wide increase in the deployment of `high speed rails(HSRs)`
> 
> China contriutes more than 0.6 of the world's HSR network in length.
> 
> There is an increasing need for acceptale quality of network services in high speed mobility scenarios.

---

> Traditional signle-path transmission declines significanlty under such extremely high speed mobility because of performance degradation.Multi-path with muptiple carriers may be able to enhance the performance.
> 
> MPTCP is a relatively mature solution to support multi-path transmission. MPTCP has already been implemented in Linux kernel and used in iOS.
>The principle of MPTCP is to enhance both efficiency and robustness.

---

### Two Questions to be answered:
> <b> Q1: Is there a significant difference in handoff time among various carriers covering HSR lines?</b>
> 
> <b> Q2: If handoff time is different among various carriers, does MPTCP perform as expected,showing a significant advantage over TCP?</b>
> 
### Answer:

During a 22-month period, we accumulated a mileage of 82,266 km, over twice of the equatorial circumference of the earth, collecting nearly 2.8 TB of data.

-  We find that the probability that both Carriers M and U suffer a handoff at the same time is nearly 0
-  As expected, MPTCP shows a significant advantage in robustness.
-  However, unexpectedly, MPTCP’s advantage in efficiency is far from satisfactory.
-  We find that mice and elephant MPTCP flows show low efficiency for different reasons.