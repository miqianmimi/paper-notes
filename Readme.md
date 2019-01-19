<h1 align="center"> Directory </h1>

### Friends, not Foes - Synthesizing Existing Trnasport Strategies for Data Center Networks
* Author: Ali Munir (Michigan State University)
* Index: SIGCOMM 2014
* Reading date: 3/12/2018
* Keywords : Datacenter transport; Congestion Control 

Many Data Center transports have been proposed in recent times. Contrary to the common perception that they are competitors. We claim that the underlying strategies used in these protocols are , in fact complementary.

So we design `PASE` a transport framework that synthesize existing transport strategies, namely, self-adjusting endpoints (used in TCP style protocols), in-network prioritization (used in pFabric), and arbitration(used in PDQ). PASE is deployment friendly It does not require any changes to the network fabric. Its performance is better than state-of-the-art protocols (pFabric). Using NS2 simulation and testbed experiments.

* [:heart_decoration: Read More](https://miqianmimi.github.io/2018/12/03/PASE/)

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

* [:heart_decoration: Read More](https://miqianmimi.github.io/2018/12/07/CC-BLOG/)


---

### DCQCN -- Congestion Control for Large-Scale RDMA Deployments
* Author: Yibo Zhu (Microsoft;ByteDance)
* Index: SIGCOMM 2015
* Reading date: 02/01/2019-10/01/2019
* Keywords : Datacenter transport; RDMA; PFC; ECN; Congestion Control 

This is for `[RDMA Section]` paper 1. Aiming at reviewing the classical paper in relative to RDMA. so i choose it due to its high reference in the filed of Datacenter transport. 

This paper in one word, proposing a new way of congestion control to solve the head-of-line blocking and unfairness problem introduced by PFC. This way is very suitable for the RDMA Datacenter and works well with RoCEv2. 

* [:heart_decoration: Read More](https://miqianmimi.github.io/2019/01/11/DCQCN/)

---

### Stream-based ML for Network Security and Anomaly Detection
* Author: Pavol Mulinka (CTU Czech)
* Index: SIGCOMM 2018 Workshop
* Reading date: 15/01/2019
* Keywords : Machine Learning; Computing methodologies; Security and Privacy.

This paper is about `Data Stream Machine Learning` for `network security and anomaly detection`. And especially for `on-line` questions (in this field the general approach is still off-line learning problem). The experiment result shows that the `adaptive random forests and stochastic gradient descent` models are able to keep up with important `concept drifts` by keeping high accuracy. 

They also introduced Big-DAMA, a big data analytics framework for large scale network traffic monitoring and analysis. 

* [:heart_decoration: Read More](https://miqianmimi.github.io/2019/01/16/Stream-based-ML/)

---

### Improving TCP Congestion Control with Machine Intelligence
* Author: Yiming Kong (Georgia Tech)
* Index: SIGCOMM 2018 Workshop
* Reading date: 16/01/2019
* Keywords : Network-> Transport protocols Computing methodologies→ Supervised learning; Reinforcement learning; Machine Learning; Security and Privacy.

This paper is about both off-line and on-line TCP-CC scheme.The writer use both supervised learning and reinforcement learning to train two TCP CC schemes.She use NS2 simulation to prepare for the dumbbell topology network and She set the environment to the basic under-buffered bottleneck network.
Why i choose this paper to read in detail is because it goes into details about the TCP-CC-ML scheme And that helps me to playback the experiment in the paper.


* [:heart_decoration: Read More](https://miqianmimi.github.io/2019/01/19/TCP-CC-ML/)

---
