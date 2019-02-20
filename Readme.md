<h1 align="center"> Directory </h1>

![Progress](http://progressed.io/bar/18?title=done)  ![](https://img.shields.io/github/last-commit/miqianmimi/paper-notes.svg?colorB=pink&logoColor=pink&style=flat)  ![](https://img.shields.io/github/followers/miqianmimi.svg?label=My%20Followers&logoColor=pink&style=social)

### Xavier: A Reinforcement-Learning Approach to TCP Congestion Control
* Author: [Akshay Aggrawal](https://www.akshayagrawal.com/)
* Index: CS211 Final Project
* Reading date: 18/02/2019
* keywords: CC , RL , NS2

In this paper, i present **Xaiver**, a congestion control policy informed by reinforcement learning and a first step towards adaptible control and analyze its perfromance on two simulated network topologies. Experimental results hint at the utility of using reinforcement-learning for congestion control while also revealing difficulites entailed by doing so. 

* [:heart_decoration: Read More](https://miqianmimi.github.io/2019/02/19/xavier/)

---

### PCC-244 X 3 : PCC Shallow Queues and Fairness / PCC fairness and flow completion time / Re-architectingg CC for high performance
* Author: Stanford Students
* Index: [🐣](https://reproducingnetworkresearch.wordpress.com/)
* Reading date: 17/02/2019
* Keywords: PCC

These three papers are PCC related. The reason why i read these three paper is for their experiment settings. 

Following are what they got for the key insights: 

- 1.PCC performance degrades in virtual environments under certain conditions. However even in the environments multiple PCC flows show significantly greater stable convergence and faireness when compared with typical TCP flows.

- 2.What the authors found was that PCC outperforms specially-engineered TCP algorithms in multiple scenarios on a variety of metrics which proves the merit of PCC and the lacking of TCP in specific scenarios. PCC has faster and better convergence to flow-fairness, as seen in figures 6, 12, and 13, and it utilizes buffers better, as seen in figures 4 and 7. What the latter result implies is that it is possible to build routers with very limited memory. Furthermore, in figure 15 we can see that in the worst-case these results are not achieved in the expense of short flow completion time as, even though PCC is slower than CUBIC, it is only 20% slower in the worst case.

- 3.PCC with the default utility function indeed does provide far better throughput than TCP in suboptimal network conditions. However, it also is very unfriendly to existing TCP flows and has significant problems with operating in a virtualized setting that shares tenancy. We discuss the tradeoffs and offer our critique below.

* [:heart_decoration: Read More](https://miqianmimi.github.io/2019/02/17/pcc-244/)

---

### QUIC：Quick UDP Internet Connections 
* Author: Google
* Reading date : 16/02/2019
* Keywords : protocol

QUIC(Quick UDP Internet Connections) is a new transport protocol for the internet, developed by Google. QUIC solves a number of transport-layer and application-layer problems experienced by modern web applications, while requiring little or no change from application writers. 

QUIC is very similar to TCP+TLS+HTTP2, but implemented on top of **UDP**. Having QUIC as a self-contained protocol allows innovations which aren't possible with existing protocols as they are hampered by legacy clients and middleboxes.

Key advantages of QUIC over TCP+TLS+HTTP2 include:
● Connection establishment latency
● Improved congestion control
● Multiplexing without head-of-line blocking
● Forward error correction
● Connection migration

* [:heart_decoration: Read More](https://miqianmimi.github.io/2019/02/16/quic/)

---


### Indigo : in the paper of panetheon  
* Author: Francis Y. Yan†, (Stanford University)
* Index: Best Paper at USENIX ATC 2018
* Reading date : 15/02/2019
* Keywords : Congestion Control, Machine Learning

Indigo is a machine-learned congestion-control scheme whose design we extract from data gathered by Pantheon.Pantheon's calibrated emulators provide an alternative: they are reproducible, can be instantiated many times in parallel. Our high-level strategy is to train Indigo using emulators, then evaluate it in the real world using Pantheon.

Pantheon facilitates realistic offline training and testing by providing a communal benchmark, evolving dataset, and calibrated emulators to allow approximately realistic offline training and testing.

* [:heart_decoration: Read More](https://miqianmimi.github.io/2019/02/15/indigo/)

---


### Research Statement  ☀
* Author: [Junchen Jiang](https://people.cs.uchicago.edu/~junchenj/) (CMU,Computer Science at The University of Chicago AP)
* Index: Thesis
* Reading date : 12/02/2019
* Keywords : Video Streaming, Future research

'Eyeball economy' is dominated by applications such as video streaming and VoIP, maintaining high user-perceived QoE(Quality of Experience) has become crucial to ensure high user engagement. recent research shows even one short buffering interruption leads to 0.39 less time. They either require costly **re-architecting of the network** core or use suboptimal **endpoint-based protocols** to react to the dynamic Internet performance based on limited knowledgge of the network.

Author demonstrate that data-driven techniques can improve Internet QoE by utilizing a centralized real-time view of performance across millions of endpoints(clients). Work focus on **two fundamental challenges** that are unique to applying data-driven approaches in networking: 

1. the need for expressive models to capture complex factors affecting QoE 
2. the need for scalable platforms to make real-time decisions with fresh data from geo-distributed clients.

Author address these challenges by integrating several domain-specific insights in networked applications with ML algorithms and systems. And achieve better QoE than using off-the-shelf machine learning solutions.




* [:heart_decoration: Read More](https://miqianmimi.github.io/2019/02/12/Thesis/)

---

### Online Flow Size Prediction for Improved Network Routing  ☀ kai ☀ 
* Author: [Pascal_Poupart_(Waterloo)](https://cs.uwaterloo.ca/~ppoupart/), Li Chen(HKUST),Kai Chen (HKUST)
* Index: ICNP 2016
* Reading date : 15/02/2019
* Keywords : Networks, Online flow size prediction, Routing

ICNP (The 26th IEEE International Conference on Network Protocols)/
We describe an emergint application o data mining in the context of computer networks. This application concerns the problem of predicting the size of a flow and detecting elephant flows(very large flows). Flow size is a very important statistic that can be used to improve routing, load balancing and scheduling in computer networks. 

Flow size prediction is particularly challenging since flow patterns continuously change and predictions must be done in real time (milliseconds) to avoid delays.

We evaluate the accuracy of three online predictors based on neural networks, Gaussian process regression and online Bayesian Moment Matching on three datasets of real traffic.

We also demonstrate how to use such online predictors to improve routing (i.e., reduced flow completion time) in a network simulation.


* [:heart_decoration: Read More](https://miqianmimi.github.io/2019/02/11/Flow-Size-Prediction/)

---

### RTC: Robust Network Traffic Classification ☀
* Author: [Junchen Jiang](https://people.cs.uchicago.edu/~junchenj/) (CMU,,Computer Science at The University of Chicago AP)
* Index: NSDI 2016
* Reading date : 11/02/2019
* Keywords : Video Streaming, Bitrate Adaption 



* [:heart_decoration: Read More](https://miqianmimi.github.io/2019/02/11/RTC/)

---

### Sibyl: A Practical Internet Route Oracle  ☀
* Author: [Junchen Jiang](https://people.cs.uchicago.edu/~junchenj/) (CMU,,Computer Science at The University of Chicago AP)
* Index: NSDI 2016
* Reading date : 11/02/2019
* Keywords : Video Streaming, Bitrate Adaption 

Network operators measure Internet routes to troubleshoot problems, and researchers measure routes to characterize the Internet. However they still rely on decades-old tools like traceroute, BGP route collectors and looking Glasses.

This paper presents Sibyl, a system that takes rich queries that researchers and operators express as regular expressions, then issues and returns traceroutes that match even if it has never measured a matching path in the past.

There are 3 steps:

1. to maximize its coverage of Internet routing, Sibyl integrates together diverse sets of traceroute vantage points that provide complementary views.

2. Users may not know which measurements will traverse paths of interest.

3. Sibyl optimizes across concurrent queries to decide which measurements to issue given resource constraints.


* [:heart_decoration: Read More](https://miqianmimi.github.io/2019/02/11/Sibyl/)

---

### MLinSDN: Machine Learning in Software Defined Networks: Data Collection and Traffic Classification  ☀
* Author: [Junchen Jiang](https://people.cs.uchicago.edu/~junchenj/) (CMU,,Computer Science at The University of Chicago AP)
* Index: NSDI 2016
* Reading date : 11/02/2019
* Keywords : Video Streaming, Bitrate Adaption 



* [:heart_decoration: Read More](https://miqianmimi.github.io/2019/02/11/MLinSDN/)

---

### DeepRM: Resource Management with Deep Reinforcement Learning  ☀
* Author: [Junchen Jiang](https://people.cs.uchicago.edu/~junchenj/) (CMU,,Computer Science at The University of Chicago AP)
* Index: NSDI 2016
* Reading date : 11/02/2019
* Keywords : Video Streaming, Bitrate Adaption 



* [:heart_decoration: Read More](https://miqianmimi.github.io/2019/02/11/DeepRM/)

---


### Pytheas: Enabling Data-Driven Quality of Experience Optimization Using Group-Based Exploration-Exploitation  ☀
* Author: [Junchen Jiang](https://people.cs.uchicago.edu/~junchenj/) (CMU,,Computer Science at The University of Chicago AP)
* Index: NSDI 2016
* Reading date : 11/02/2019
* Keywords : Video Streaming, Bitrate Adaption 

Continuing with the Sequence 3. 

Many ways of optimizing Quality of Experience (QoE) are using data-driven mechanisms. they use the recent sessions 's QoE result to do the optimal decisions. However, they are not accurate and incomplete due to: 
(1) suffer from many known biases (2) cannot respond to sudden changes.

the author think that the **Drawing a parallel from machine learning**, data-driven QoE optimization should instead be cast as a **real-time exploration and exploitation** (E2) rather than as a prediction problem. Adopting E2 in network applications, however, introduces key architectural challenge and algorithm challenge.

We present Pytheas, a framework which addresses these challenges using a group-based E2 mechanism. The insight is that application sessions sharing the same features can be grouped so that we can run E2 algorithms at a per-group granularity.Using an end-to-end implementation and a proof-of-concept deployment in CloudLab, We show that Pytheas improves video QoE 

* [:heart_decoration: Read More](https://miqianmimi.github.io/2019/02/11/Pytheas/)

---

### CFA: A Practical Prediction System for Video QoE Optimization  ☀
* Author: [Junchen Jiang](https://people.cs.uchicago.edu/~junchenj/) (CMU,,Computer Science at The University of Chicago AP)
* Index: NSDI 2016
* Reading date : 11/02/2019
* Keywords : Video Streaming, Bitrate Adaption 

Continuing with the Sequence 2. 

Many prior efforts have suggested that internet video QoE could be dramatically improved by using data-drive prediction of video quality for different choices. (e.g, CDN  or bitrate) to make optimal decisions.
model to expressive enouggh to capture these complex relationships and capble of updating quality predictions in near real-time. 
We design and implement CFA(Critical Feature Analytics). This is driven by domain-specific insights hat video quality is typically determined by a small subset of critical features whose criticality persists over several tens of minutes.

learn critical features for different sesions on coarse-grained timescales.

Using a combination of a real-world pilot deplyment and trace-driven analysis. we demonstrate that CFA leads to significant improvements in video quality. 32% less buffering time and 12% higher bitrate than a random decision maker.


* [:heart_decoration: Read More](https://miqianmimi.github.io/2019/02/11/CFA/)

---

### CS2P: Improving Video Bitrate Selection and Adaptation with Data-Driven Throughput Prediction ☀

* Author: [Yi Sun](http://people.ucas.edu.cn/~sunyi) ( CMU Visitor 中科院(UCAS)AP )
* Index: Sigcomm 2016
* Reading date : 11/02/2019
* Keywords : Internet Video, TCP, Throughput Prediction, Bitrate Adaption, Dynamic Adaptive Streaming over HTTP(DASH)

Continuing with the Sequence 1.

Bitrate adaptation is critical to ensure good quality-of-experience(QoE) for Internet Video.（1) initial bitrate selection lower startup delay and offer high initial resolution (2) mid-stream bitrate adaption for high QoE. Prior efforts did not systematically quantify real-world throughput predictability or develop good prediction algorithms. To bridge this gap, the paper do three contributions:

>1. Sessions sharing similar key features present similar initial throughput values and dynamic patterns
>2. There is a natural "stateful" behavior in throughput variability within a given session 

with these insights, we build CS2P, a throughput prediction system which use a data-driven approach to learn

>1. cluster of similar sessions. 
>2. an initial throughput predictor.
>3. a Hidden-Markov-Model based midstream predictor modeling the stateful evolution of throughput.

we develop a prototype system and show using trace-driven simulation and real-world experiments that:(1) CS2P outperforms existing prediction approaches (2) CS2P achieve improvement on overall QoE and high average bitrate over state-of-art model predictive conrol(MPC).

 
* [:heart_decoration: Read More](https://miqianmimi.github.io/2019/02/11/CS2P/)

---


### DBA: Routing or Computing? The Paradigm Shift Towards Intelligent Computer Network Packet Transmission Based on Deep Learning ☀

* Author: Bomin Mao (Tohoku University 日本東北大學 )
* Index: `Journal` | IEEE Transactions on Computers 2017
* Reading date : 10/02/2019
* Keywords : Software defined routers, network traffic control, deep learning, backbone networks, routing.
 
> 1. Software Defined Routers (programmable routers) have emerged as a viable solution. 
> 2. Multi-core platforms significantly promote SDRs' parallel computing capacities, enabling them to adopt artificial intelligent techniques. i.e., deep learning, to manage routing paths.

In this paper, we explore the deep learning based route estimation for high-throughput packet processing under the GPU-accelerated SDRs.We envision a supervised deep learning system to construct the routing tables. We show how the proposed method can be integrated with programmable routers using both (CPUs) and (GPUs).we proposed DBA(deep belief architecture) to predict the next nodes. In particular, the simulation results demonstrate that our proposal outperforms the benchmark method in terms of delay, throughput, and signaling overhead.

* [:heart_decoration: Read More](https://miqianmimi.github.io/2019/02/10/DBA/)

---


### PCC Vivace: Online-Learning Congestion Control ☀

* Author: Mo Dong and Tong Meng (UIUC)
* Index: NSDI 2018
* Reading date : 10/02/2019
* Keywords : congestion control, reinforcement learning
 
Continuing with the Sequence 2.

Author leverage ideas from the rich literature on online (convex) optimization in machine learning to design Vivace, a novel rate-control protocol, designed within the recently proposed PCC framework. PCC Vivace outperforms the previous realization of the PCC framework, and BBR in terms of performance (throughput, latency, loss), convergence speed, alleviating bufferbloat, reactivity to changing network conditions, and friendliness towards legacy TCP in a range of scenarios. Vivace requires only sender-side changes and is thus readily deployable.

* [:heart_decoration: Read More](https://miqianmimi.github.io/2019/02/10/PCCvivace/)

---


### PCC:Re-architecting Congestion Control for Consistent High Performance ☀

* Author: Mo Dong (UIUC)
* Index: NSDI 2015
* Reading date : 10/02/2019
* Keywords : congestion control, reinforcement learning
 
Continuing with the Sequence 1.

Add [pcc](http://modong.github.io/pcc-page/#pcc_arch) website

TCP has little hope of achieving high performance due to fundamental architectural deficiency. Propose PCC(Peformance-oriented Congestion Control) PCC in which each sender continuously observes the connection between its actions and empricially experienced performance, enabling it to consistently adopt actions that result in high performance. We prove that PCC convereges to a stable and fair equilibrium.

* [:heart_decoration: Read More](https://miqianmimi.github.io/2019/02/10/PCC/)

---

### Remy: Tcp ex Machina: Computer-Generated Congestion Control ☀

* Author: Keith Winstein, Hari Balakrishnan (MIT Now is already Stanford's AP teaching CS244)
* Index: Sigcomm 2013
* Reading date : 10/02/2019
* Keywords : congestion control, computer-generated algorithms.
 
Although i already heard about Remy on the group meeting, but there is no reason to skip it. Since the algorithm used inside the paper is so RL-like.

This paper describe a new apparoach to end-to-end congestion control on a multi-user network. We developed a program called Remy that generates contestion-conrol algorithms to run at the endpoints. Remy produces A distributed algorithm to achieve high throughput and low queueing delay.

In simulations with ns-2, Remy-generated algorithms outperformed human-designed end-to-end techniques, including TCP Cubic, Compound and Vegas. Remy performs better than algorithms in parameters known as priori(datacenter);prior knowledgeg is less precise(cellular network); estimate the sensitivity of the resulting performance to the specificity of the prior knowledge.

* [:heart_decoration: Read More](https://miqianmimi.github.io/2019/02/10/Remy/)

---

### Pensieve: Neural Adaptive Video Streaming with Pensieve ☀

* Author: [Hongzi Mao](http://people.csail.mit.edu/hongzi/) (MIT Computer Science and Artificial Intelligence Laboratory)
* Index: Sigcomm 2017
* Reading date : 09/02/2019
* Keywords : bitrate adaptation, video streaming, reinforcement learning
 
Client-side video players employ ABR algorithms to optimize user QoE. However, state-of-the-art ABR algorithms suffer from limitation: use fixed control rules based on simplified or inaccurate models of the deployment environment. We propose Pensieve, a system that generates ABR alggorithms using reinforcement learning (RL). Pensieve trains a neural network model hat selects bitrates for future video chunks based on observations collected by client video players. No matter that it outperforms the state-of-the-art scheme.

* [:heart_decoration: Read More](https://miqianmimi.github.io/2019/02/09/Pensieve/)

---

### PICC: Proactive Incast Congestion Control in a Datacenter Serving Web Application ☀

* Author: Haoyu Wang (UVA University of Virginia)
* Index: Infocom 2018
* Reading date : 08/02/2019
* Keywords : Congestion Control, Web application
 
I read this paper because it is Infocom 2018 conference paper and it is about congestion control. But i have to say this paper's abstraction is not so good for reading.

With rapid development of web applications in datacenter, network latency becomes more important to user experience.The network latency will be greatly increased by incast congestion, in which a huge number of requests arrive at the front-end server simultaneously. This is an incast problem. Previous incast problem solutions are usually not efficient. In this paper, PICC (Proactive Incast Control System) is proposed. It limits the number of data servers concurrently connected to the front-end server to avoid the incast contestion through data placement.PICC incorporate a queuing delay reduction algorithm that assigns higher transmission priority to data objects with smaller size and longer queuing times.

* [:heart_decoration: Read More](https://miqianmimi.github.io/2019/02/08/PICC/)

---

### CCP:Restructuring Endpoint Congestion Control ☀

* Author: Akshay Narayan (MIT Computer Science and Artificial Intelligence Laboratory)
* Index: Sigcomm 2018
* Reading date : 08/02/2019
* Keywords : Congestion Control, Operating System

This paper is very special idea contained. What it does is a unite thought. It describes the implementation and evaluation of a system to implement complex congestion control functions by placing them in a separate agent outside the datapath (which means Linux Kernel TCP, UDP-based QUIC, kernel-bypass transports like mTCP-on-DPDK) these datapath is for the information about packet rtt and ECN, losses. now we call this off-datapath system Congestion Control Plane(CCP). "write once, run anywhere" makes it supereasy.

* [:heart_decoration: Read More](https://miqianmimi.github.io/2019/02/08/ccp)

---


### Jellyfish: Networking Data Centers Randomly

* Author: Ankit Singla (University of Illinois at Urbana–Champaign)
* Index: HotCloud 2011
* Reading date : 31/01/2019
* Keywords : network topology

This paper is for the DataCenter Networking structure, because the datacenter needs high bandwidth requirement. So itself naturally to incremental expansion. Suprisingly, the Jellyfish is more cost-efficient than a fat-tree.
25% more servers at full capacity using the same equipment at the scale of a few thousand nodes, and this advantage improve with scale.
I learn what is HotCloud and the first sample reproducing.

* [:heart_decoration: Read More](https://miqianmimi.github.io/2019/01/31/jellyfish/)

---


### Pantheon: the training ground for Internet congestion-control research ☀

* Author: Francis Y. Yan†, (Stanford University)
* Index: Best Paper at USENIX ATC 2018
* Reading date : 27/01/2019
* Keywords : Congestion Control

The author present the [Pantheon](https://pantheon.stanford.edu), a system taht addresses this by serving as a community " training ground " for research on Internet Protocols and congestion control. There is a common set of benchmark algorithms and a shared evaluation platform, and a public archive of results.
Pantheon can also be used to develop new CC schemes , two of which already published on NSDI 2018. I think this is mysterious and interesting that's why i choose this paper to read.

* [:heart_decoration: Read More](https://miqianmimi.github.io/2019/02/09/Pantheon/)

---

### ECN or Delay: Lessons Learnt from Analysis of DCQCN and TIMELY

* Author: Yibo Zhu (Microsoft;ByteDance)
* Index: CoNEXT 2016 
* Reading date : 20/01/2019
* Keywords : Datacenter transport, RDMA, ECN, delay-based, congestion control

This is also for `[RDMA Section]` paper 2. Aiming at reviewing the classical paper in relative to RDMA. Based on the paper name, we already know that this paper is about the compare of `DCQCN` and `TIMELY`. 

According to the YiboZhu, which is the author of the `DCQCN`: DC networks especially drop-free RoCEv2 networks require efficient cc protocols. `DCQCN(ECN-based)` and `TIMELY(delay-based)` are two recent proposals for this purpose. In this paper, we analyze DCQCN and TIMELY using fluid models and simulations, for stability, convergence, fairness and flow completion time. We uncover several surprising behaviors of these protocols. 

The author also address the broader question: are there fundamental reasons to `prefer either ECN or delay` for end-to-end congestion control in DC Networks ?

* [:heart_decoration: Read More](https://miqianmimi.github.io/2019/01/22/ECN-or-DELAY/)

---

### TIMELY: RTT-based Congestion Control for the DataCenter 

* Author: Radhika Mittal (UC Berkeley)
* Index: SIGCOMM 2015 
* Reading date : 20/01/2019
* Keywords : Datacenter transport, delay-based CC, OS-bypass, RDMA

This is for `[RDMA Section]` paper 2. Aiming at reviewing the classical paper in relative to RDMA. 

Datacenter transports aim to deliver low latency messageing together with high throughput. We show that simple packet delay, measured as `round-trip times` at hosts, is an effective congestion signal without the need for switch feedback. 

- First, we show that advances in NIC hardware have made RTT measurement possible with microsecond accuracy, and that these RTTs are sufficient to estimate switch queueing. 
- Then we describe how TIMELY can adjust transmission rates using RTT gradients to keep packet latency low while delivering high bandwidth. 

TIMELY is the first delay-based CC protocol in datacenter. And it achieves its result despite having an order of magnitude fewer RTT signals.

* [:heart_decoration: Read More](https://miqianmimi.github.io/2019/01/20/TIMELY/)

---

### Learning Network by Reproducing Network Result 🦄
* Author: Lisa Yan (Stanford University)
* Index: SIGCOMM 2017 
* Reading date : 19/01/2019
* Keywords : Reproducible research, Teaching computer networks
* Score: 📒📕📘📗

This paper is finished by my Academic Idol Lisa Yan. This paper is so important because [Hope](http://web.stanford.edu/class/cs244/index.html) is a waking [dream](https://reproducingnetworkresearch.wordpress.com/page/2/)．

    I'd like to deal with this course as a student.
    I'd like to do the final pj of this course.

Lisa Yan said that:
> "In the past five years, the graduate networking course at Stanford has assigned over 200 students the task of reproducing results from over 40 networking papers. We began the project as a means of teaching both engineering rigor and critical thinking, qualities that are necessary for careers in networking research and industry. We have observed that reproducing research can simultaneously be a tool for education and a means for students to contribute to the networking community. "

* [:heart_decoration: Read More](https://miqianmimi.github.io/2019/01/20/Reproducing-Network/)

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

### Stream-based ML for Network Security and Anomaly Detection
* Author: Pavol Mulinka (CTU Czech)
* Index: SIGCOMM 2018 Workshop
* Reading date : 15/01/2019
* Keywords : Machine Learning; Computing methodologies; Security and Privacy.

This paper is about `Data Stream Machine Learning` for `network security and anomaly detection`. And especially for `on-line` questions (in this field the general approach is still off-line learning problem). The experiment result shows that the `adaptive random forests and stochastic gradient descent` models are able to keep up with important `concept drifts` by keeping high accuracy. 

They also introduced Big-DAMA, a big data analytics framework for large scale network traffic monitoring and analysis. 

* [:heart_decoration: Read More](https://miqianmimi.github.io/2019/01/16/Stream-based-ML/)

---

### DCQCN -- Congestion Control for Large-Scale RDMA Deployments
* Author: Yibo Zhu (Microsoft;ByteDance)
* Index: SIGCOMM 2015
* Reading date : 02/01/2019-10/01/2019
* Keywords : Datacenter transport; RDMA; PFC; ECN; Congestion Control 

This is for `[RDMA Section]` paper 1. Aiming at reviewing the classical paper in relative to RDMA. so i choose it due to its high reference in the filed of Datacenter transport. 

This paper in one word, proposing a new way of congestion control to solve the head-of-line blocking and unfairness problem introduced by PFC. This way is very suitable for the RDMA Datacenter and works well with RoCEv2. 

* [:heart_decoration: Read More](https://miqianmimi.github.io/2019/01/11/DCQCN/)

---

### Congestion Control Something to say
* Blog Conclusion of Congestion Control
* Reading date : 7/12/2018
* Keywords : Congestion Control ; Reinforcement Learning

I find a NYC coder's Blog in which it introduced several important concept in Congestion Control. Also with several useful code. So I read his 4 blogs and conclude his words. These 4 blogs are the introduction of CC, the Cubic , the RED , the Reinforcement Learning .

* [:heart_decoration: Read More](https://miqianmimi.github.io/2018/12/07/CC-BLOG/)

---

### Exising TCP CC Algorithm
* Summary of Congestion Control
* Reading date : 5/12/2018
* Keywords : TCP ; Congestion Control 

TCP Congestion Control aims at choose a strategy to find the appropriate cwnd and to acheive the best utility of bandwidth. In this summary, we briefly introduce several different mechanism in TCP CC Algorithm starting from TCP Vegas , TCP Reno , Cubic, BBR and Remy.

* [:heart_decoration: Read More](https://miqianmimi.github.io/2018/12/06/TCP-CC/)

---

### Friends, not Foes - Synthesizing Existing Trnasport Strategies for Data Center Networks
* Author: Ali Munir (Michigan State University)
* Index: SIGCOMM 2014
* Reading date : 3/12/2018
* Keywords : Datacenter transport; Congestion Control 

Many Data Center transports have been proposed in recent times. Contrary to the common perception that they are competitors. We claim that the underlying strategies used in these protocols are , in fact complementary.

So we design `PASE` a transport framework that synthesize existing transport strategies, namely, self-adjusting endpoints (used in TCP style protocols), in-network prioritization (used in pFabric), and arbitration(used in PDQ). PASE is deployment friendly It does not require any changes to the network fabric. Its performance is better than state-of-the-art protocols (pFabric). Using NS2 simulation and testbed experiments.

* [:heart_decoration: Read More](https://miqianmimi.github.io/2018/12/03/PASE/)

---


