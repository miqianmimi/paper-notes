<h1 align="center"> Directory </h1>

### Friends, not Foes - Synthesizing Existing Trnasport Strategies for Data Center Networks
* Author: Ali Munir (Michigan State University)
* Index: SIGCOMM 2014
* Reading date: 3/12/2018
* Keywords : Datacenter transport; Congestion Control 

Many Data Center transports have been proposed in recent times. Contrary to the common perception that they are competitors. We claim that the underlying strategies used in these protocols are , in fact complementary.

So we design `PASE` a transport framework that synthesize existing transport strategies, namely, self-adjusting endpoints (used in TCP style protocols), in-network prioritization (used in pFabric), and arbitration(used in PDQ). PASE is deployment friendly It does not require any changes to the network fabric. Its performance is better than state-of-the-art protocols (pFabric). Using NS2 simulation and testbed experiments.

* [:heart_decoration: Read More](https://miqianmimi.github.io/2018/12/03/PASE/#more)

---


### Exising TCP CC Algorithm
* Summary of Congestion Control
* Reading date: 5/12/2018
* Keywords : TCP ; Congestion Control 

TCP Congestion Control aims at choose a strategy to find the appropriate cwnd and to acheive the best utility of bandwidth. In this summary, we briefly introduce several different mechanism in TCP CC Algorithm starting from TCP Vegas , TCP Reno , Cubic, BBR and Remy.

* [:heart_decoration: Read More](https://miqianmimi.github.io/2018/12/06/TCP-CC/)

---

### Congestion Control Something to say
* Blog Conclusion of Congestion Control
* Reading date: 7/12/2018
* Keywords : Congestion Control ; Reinforcement Learning

I find a NYC coder's Blog in which it introduced several important concept in Congestion Control. Also with several useful code. So I read his 4 blogs and conclude his words. These 4 blogs are the introduction of CC, the Cubic , the RED , the Reinforcement Learning .

* [:heart_decoration: Read More](https://miqianmimi.github.io/2018/12/07/CC-BLOG/#more)


---

### Congestion Control for Large-Scale RDMA Deployments
* Author: Yibo Zhu (Microsoft;ByteDance)
* Index: SIGCOMM 2015
* Reading date: 02/01/2019-10/01/2019
* Keywords : Datacenter transport; RDMA; PFC; ECN; Congestion Control 

This is for `[RDMA Section]` paper 1. Aiming at reviewing the classical paper in relative to RDMA. so i choose it due to its high reference in the filed of Datacenter transport. 

This paper in one word, proposing a new way of congestion control to solve the head-of-line blocking and unfairness problem introduced by PFC. This way is very suitable for the RDMA Datacenter and works well with RoCEv2. 

* [:heart_decoration: Read More](https://miqianmimi.github.io/2019/01/11/DCQCN/#more)