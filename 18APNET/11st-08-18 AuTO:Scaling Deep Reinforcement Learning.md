# AuTO:Scaling Deep Reinforcement Learning for Datacenter-Scale Automatic Traffic Optimization
* [LiChen] 
* [Keywords: Datacenter Networks, Reinforcement Learning, Traffic Optimization]

## Abstract

> ### 1. Motivation
> Traffic optimizations(TO)are very difficult online decision-making prolems.
> Previsously, They are done with heuristics relying on operators' understanding of the workload and environment.
> Encouraged by recent success in applying Deep Reinforcement Learning (DRL) techniques to solve complex online control problems.Li wants to use (DRL) to automatic TO without human-intervention. 
> 
> ### 2.Contriution
> In order to leverage the long-tail distriubtion of datacenter traffic, we develop a two-level DRL system, **AuTO**,which solve the scalaility prolem.
> 
> * [ Peripehral System(PS)] PS reside on end-hosts, collect flow information. and make TO decisions locally, with minimal delay for short flows. 
> * [ Central System(CS) ] PS is controlled by **Central System(CS)**CS further makes individual TO decisions for flows

> AuTO reduces the TO turn-around time from weeks to ~100 milliseconds. For example, it demonstrates up to 48.14% reduction in average flow completion time (FCT) over existing solutions.
 

## Introduction

 ### Present Situation:
> * [parameter-environment mismatchs]
> **PIAS**, undermismatch scenarios, performance degradation can be as much as 38.46%. **pFabric** shares the same problem when implemented with limited switch queues: for certain cases the average **FCT** can be reduced by over 30% even if the thresholds are carefully optimized.
> 
> * [Long time for designing TO heuristics]
> so we are motivated to enable DRL(deep reinforcement learning) for automatic datacenter TO.

### Hard Part:
> <b> How to enable DRL-based automatic TO at datacenter-scale ?</b>
> understand the long-tail distribution of the Datacenter traffic. Most of the flows are short flows. Most of the bytes are from long flows. long flows TO decisions takes long time to be finished.
> 
> The key to AuTO's scalability is to detach time-consuming DRL processing from quick action-taking for short flows. we adopt Multi-Level Feedback Queueing ( MLFQ ) for PS to schedule flows guided by a set of thresholds.Auto has different DRL algorithm for long flows and short flows.
> 
### Effective :
Only 8 hours of training ,AuTO acheives 8.71% reduction in average (9.18%) in tail FCT compared to heuristics.

