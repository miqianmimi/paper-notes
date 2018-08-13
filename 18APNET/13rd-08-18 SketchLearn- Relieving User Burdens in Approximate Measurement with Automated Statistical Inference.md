# SketchLearn: Relieving User Burdens in Approximate Measurement with Automated Statistical Inference
* [Qun Huang] 
* [Keywords: Sketch, Network measurement]

## Abstract

> ### 1.Background
> Network measurement is challenged to fulfill stringent resource requirements in the face of massive network traffic. While approximate measurement can trade accuracy for resource savings, it demands intensive manual efforts to configure the right resource-accuracy trade-offs in real deployment. 

> Existing approximate measurement approaches inherently deal with resource conflicts when tracking massive network traffic with limited resources.

> ### 2.Contribution
> We design **SketchLearn**, a novel sketch-based measurement framework that resolves resource conflicts by learning their statistical proeprties to elimnate conflicting traffic components.

> We prototype **SketchLearn** on OpenVSwitch and P4, and our tested experiments and stress-test simulation show that SketchLearn automatically monitor traffic statistics and effectively supports network-wide measurement with limited resources.

## Introduction

>  Unfortunately, measuring traffic statistics is non-trivial in the face of massive network traffic and large-scale net-work deployment.
>  
>  Error-free measurement requires per-flow tracking, yet today's data center networks can have thousands of concurrent flows in a very small period from 50ms down to even 5ms. This would require tremendou resources for performing per-flow tracking.

> resource constraints => many approaches in the literature leverage approximation techniques to trade between **resource usage** and **measurement accuracy**.
> 
> * sampling
> 
> * top-k counting
> 
> * sketch-based approaches
> 
> <b>Tight binding between resource configurations and accuracy parameters => </b>
> * (1) Adminstrator need to specify tolerable error levels as input for resouce configurations
> 
> * (2) each configuration is tied to specific parameters 
> 
> * (3) provide only worst-case analysis and fails to guide the resource configurations based on actual workloads.

---

<b> We address the issue by focusing on sketch measurement,fully records the chosen statistics of all observed packets in fixed-size data structures.</b>

Its `idea` is to characterize the inherent statistical properties of resource conflicts in sketches rather than pursue a perfect resource configuration to mitigate resource conflicts.

We prototype `SketchLearn` atop OpenVSwitch and P4 to show its feasibility of being deployable in both software and hardware switches, respectively.

## Motivation
Start with measuring `per-flow frequencies` of network traffic across time intervals called `epochs`.

Based on per-flow frequencies, we can derive sophiscated traffic statistics ,such as <b>heavy hitters, heavy changers, superspread and DDoS cardinality, flow size distribution and entropy.</b>

