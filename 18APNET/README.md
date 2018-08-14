
This MarkDown is what I learned about the state-of-the-art of Network from 2018 2nd APNet and from other students and alumnis in Prof.Kai Chen's Group. <b>I will keep on updating this summary after other group members upload their summaries.</b>

`Author`: [Yiqing Ma](https://github.com/miqianmimi)

`Main Website`: [ APNET web](https://conferences.sigcomm.org/events/apnet2018/index.html)

`My Summary of SIGCOMM Talks`📘 =>  [APNET SIGCOMM Talks Summary ](https://github.com/miqianmimi/paper-notes/tree/master/18APNET)

---

# KeyNote Talk
### Towards Self-Running Networks? Some Thoughts on the Role of Machine Learning/AI in Future Networking.
`Zhi-Li Zhang` - `Professor at University of Minnesota`

#### Brief Summary:

Today's internet is primarily an information delivery platform. Vast Cloud computing infrastructures and huge data centers at the backend and geotraphically dispersed content distribution networks at the frontend/edge have evolved to support massive information delivery services.

There are two new trends in networking :

* Software-defined networking(SDN)

* Network funciton virtualization(NFV)

These have further given rise to the bold vision of “self-running” or “self-driving” networks.

we will highlight some of our research work on applying machine learning techniques to manage complex networks as well as on advancing the state-of-art in SDN and NFV.
 
Based on our experience in applying machine learning and AI techniques in network management, we will share some personal thoughts on the challenges and initial steps we may take in working towards the vision of “self-running” networks.

---

#### Supplementary:

SDN means an approach to cloud computing that facilitates network management and enables programmatically efficient network configuration in order to improve network performance and monitoring.

NFV means a network architecture concept that uses the technologies of IT virtualization to virtualize entire classes of network node functions into building blocks that may connect, or chain together, to create communication services.

---

> `Bojie Li:`
> 
> Internet 已经从客户-服务端下载模型成功演化成了云+CDN+端的复杂模型，未来将从人的互联扩展到物的互联。SDN把网络从Imperative变成了declaractive,随着网络中产生大数据，将需要AI来做出智能决策，让网络自动运行，适应不断变化的应用需求，解放运维人员，一方面：延续Google用AI加速数据结构等研究，用AI来替代系统中的固定策略，提升动态网络系统的效率。另一方面，除了性能，安全和故障恢复，用AI来提升和演进网络架构和策略。听过的提问的时间最长的keynote,讨论非常激烈：目前网络和系统的策略有理论基础，AI靠不靠谱？为什么用deep learning?网络能不能反过来加速AI的进步？
>
---

> `Yunan Zhang:`
>   
> AS AI has shown super perfomance in many areas such as image, vision, speech recognition, games..., we should think deeper on "AI in networking".
> * 第一个方向是Big network -> Big data 
> 用深度学习算法提升网络性能，解放基于启发式的人力分析，
> * 第二个方向是Off-network -> In-network,是从更大的视野来看，能否利用AI提出网络架构上的演进.
> Zhili老师还分享了近期的DeepCache工作.(self-running network)
---

# Industry Talk
### 1.Toward Highly-Available Cloud Systems 
`Chuanxiong Guo`-`Director of the AI Lab of Bytedance Inc`-
[[Slides]](https://conferences.sigcomm.org/events/apnet2018/slides/cx.pptx)

#### Brief Summary：

IT companies around the globe are building large-scale cloud systems to meet the demands of an increasing number of cloud computing services. These cloud systems, however, can be brought down to their knees, by a large number, sometimes high profile, incidents. These incidents reduce cloud system availability and cost companies’ money, brand reputation, and team moral.

In this talk, I will present my on-going journey of building highly-available cloud systems, from measurement and monitoring, to failure localization and understanding, and to automatic mitigation and intervene. The goal of this journey is to build highly-available systems that recover from failures when they happen, and that avoid avoidable failures by learning from the past.

---

#### Supplementary:
Since my graduate project is to realize Chuanxiong's paper "Pingmesh: A Large-Scale System for Data Center Network Latency Measurement and Analysis" I'd like to continue contribute my power to realize the large-scale Datacenter network measurement and realize the automation of system development and design.

---

> `BoJie Li:`
> 
> 大陆SIGCOMM第一人郭传雄提出了网络系统中灰色故障的概念，即故障检测与实际应用运行的不匹配导致运维系统没发现故障，而应用运行不正常或者性能差，为此，设计了Paranoma系统来让应用end-to-end 报告粗张，以及ByteBrain 流式计算系统实现实时WAN流量的监测和调度。
> 
---
 
> `Zhuoyi Peng:`
> 
>  This system focuses on the availability of a could system and failure tolerance, using solutions from a series of aspects, which takes the advantage of its appropriate architecture. 
>
>  Building up a highly available cloud and AI -enabled system is what i really want to pursue, requiring me to imporve my engineering ability.
>
>---


### 2.Towards Converged SmartNIC Architecture for Bare Metal and Public Clouds at Tencent Scale
`Layong Luo`-`Expert Engineer (T4) at Tencent`-[[Slides]](https://conferences.sigcomm.org/events/apnet2018/slides/larry.pdf)

#### Brief Summary:

With fast increase of NIC speed and SDN policies, and unfortunately with slow increase of CPU performance, pure software based host SDN stack won't be able to keep up very soon. In the coming post Moore's Law world, specialization/hardware acceleration seems to be the only way left to close the gap between host SDN performance and NIC speed in the long run.

In this talk, He present Tencent's practice about network acceleration based on SmartNIC. Specifically, I will explain SmartNIC motivation, use cases in both bare metal and public clouds, and our vision to converge the SmartNIC architecture for bare metal and public clouds in the future. In the end, I will share our experience of building hardware from scratch in Internet company like Tencent.

---

> `Bojie Li:`
> 
> 软硬件全栈专家Larryluo介绍了腾讯SmartNIC在bare-metal云和虚拟机公有云的实践，传统上bare-metal云用ToR switch做网络功能，但交换机的灵活性和scalability都有限。公有云hypervisor软件处理虚拟化CPU开销高。结合NIC,FPGA,和CPU的SmartNIC SoC部署在两种场景中，腾讯的FPGA和办卡开发都非常敏捷。
> 
---

> `YuNan Zhang:`
> 
> 这篇是全栈专家layong luo 对Tencent的SmartNIC分别在bare-metal和Public cloud环境下的部署进行的介绍。
> Traditional bare-metal cloud use ToR switch to implement network functions, but the switch to implement network functions, but the switch scalability and flexibility are all limited. While the SMartNIC-based Virtualization in Tenent is high flexible and scalable.
> In the public cloud, the overhead of soft-ware processing on supervisor is high. While they make network acceleration with SmartNIC, all packets go through the new hypervisor in SmartNIC, making the software hypervisor lightweight,saving CPU cost.

---

> `Xinchen Wan:`
> 
> Network acceleration based on SmartNIC. Tencent uses SmartNIC in two cases: bare metal and public clouds but treats them in different way. 
> * In bare metal case, they offloaded ToR to SmartNIC, that is a bottom-to-NIC direction. 
> * And in public cloud case, offloaded hypervisor to SmartNIC which is a top-to-NIC direction. 

---

>`Zhuoyi Peng:`
>
> In Comparison to the advancement in skylake microarchitecture of Intel, the presentation of SmartNIC did arise my attention, because it has strong relation with my new work. 
> 
> Aim to offloading the CPU, **we now use GPU Direct RDMA for lower latency and high throughout data transportation**. In the future, we may integrate the technique, GPU Direct Async to move the control plane to the GPU. 
> 
> Briefly what we do is using GPU to take up some calculation tasks, which raises a question , “How can we use SmartNIC or other hardware to offload the CPU under the fact of limited improvement in CPU?”.
>
---

### 3.SONiC: Software for Open Networking in the Cloud
`Lihua Yuan`-`Partner Software Engineering Manager at Microsoft`-[[Slides]](https://conferences.sigcomm.org/events/apnet2018/slides/lihua.pdf)

#### Brief Summary:

SONiC is an open source network operating system that is widely deployed in Microsoft Azure data center as well as many partner companies. It leverages the industrial standard Switch Abstraction Interface (SAI) to work across switch ASICs from multiple companies. It features a modular design with containers. In this talk, I will present the high-level design of SONiC, share the experiences we learned from developing SONiC and deploying SONiC at scale.

---

#### Supplementary :

[SONiC](http://azure.github.io/SONiC/) is a Software for Open Networking in the Cloud.It is an open source project for network routers and switches.

Microsoft running one of the largest clouds in the world. It use best-of-breed switching hardward for the various tiers of the network, Deploy new features without impacting end users.Enable our Software-Defined Networking software to easily control all hardware elements in the network using a unified structure to eliminate duplication and reduce failures.

To address these requirements, Microsoft pioneered Software for Open Networking in the Cloud(SONiC).This is a breakthrough for network switch operations and management.SONiC is a uniquely extensible platform, with a large and growing ecosystem of hardware and software partners, that offers multiple switching platforms and various software components.

---

>`Bojie Li:`
>
>微软Azure云网络掌门Lihua-Yuan讲了Sonic,云厂商共建的白盒交换机开放社区，宜在打破交换机芯片的Vendor lock-in.提出了统一的交换机南向北向接口（Switch Abstraction Interface)和软件架构。Sonic软件不断演进，已经支持Docker的无缝热迁移。

---

>`Duowen Liu:`
>
> **What is SONiC**: It is a collection of software networking components required to build network devices with rich functionality. With SAI(switch abstraction interface) specification,`SONiC` can run on various switching platforms.It based on modular architecture and has a lean stack so that suitable for data center network. All components of SONiC are open source and have active community for developers.
> 
> **Why SONiC**:SDN has several principles such as virtualization,scale-out and centralized controllers and SONiC is based on these principles. SONiC allows us to share the same software stack across hardware from multiple switch vendors and debug, fix,test much faster.It also allow us the flexibility to develop features that are required for data center network.

> **Today’s SONiC**: Now it integrates with standardized SAI interface and allows us to exploit new hardware faster. Initial contributions of SONiC also supported open source platform drivers for certain switches enabling SONiC to run Layer2/3 switch.
> 
> **Tomorrow's SONiC**:Maybe we can try to deploy containerized applications on SONiC with docker, and manage them with kubernetes.
> 
> Some details about SONiC
> * SONiC is not a linux distribution itself. It now runs on Debian Jessie.
> * SONiC is purely a  software solution
> * SONiC is a community supported product
> 
 ---

> `Zhuoyi Peng:`
> 
> SONiC, an open source project for network routers and switches. I am sorry to say what my previous study didn’t get involved in such switch layer, but this project is of great extendibility that we can make more contribution to enrich its feature and application usage. 
> 
---


### 4.Unlocking general purposes processors to boost packet processing performance
`Cunming Liang`-`Platform Solution Architect at Intel`-[[Slides]](https://conferences.sigcomm.org/events/apnet2018/slides/cunming.pdf)

#### Brief Summary:

Fixed Network Functions are rapidly transitioning from discrete appliances into Virtual Network Functions,

this is driving the need to more efficiently consolidate compute, storage and communications workloads on a general purpose server platform. 

This presentation reviews advancements made in CPU and platform technology that enable developers to efficiently migrate communications workloads from discrete appliances to standard server platforms. 

Intel’s skylake microarchitecture and I/O subsystems will be reviewed from a packet processing perspective. 

We will also review new functionality that has been added to the DataPlane Development Kit in order to truly unlock the packet processing capabilities of the platform.

---

#### Supplementary :
Intel Skylake microarchitecture: It is core microarchitecture. and there are five-point look at what Skylake means for Intel.

1. Skylake boasts improved performance, particularly on mobile.

2. Skylake embraces next-generation graphics technologies.

3. Skylake offers superior power efficiency

---

> `BoJie Li:`
> 
> DPDK 核心开发者Cunming Liang从Skylake 微体系结构除法，讲解了DPDK如何节约处理每个数据包的指令数。首先，多发射和乱序执行需要尽量减少指令间的依赖；其次，核间总线从环形互联变成mesh互联，核间cache coherence 开销增加；第三,内存和PCle带宽提高，但Cache-miss开销仍然高，PCle小包带宽仍然是瓶颈，DPDK使用VPP等技术实现了单机1.2Tbps网络包处理。DPDK也不再仅仅是网络收发包平台，而成为了CPU与包括网卡、SSD、加速卡在内的硬件设备的高效统一通信接口，成为众多研究工作的基础平台。未来的两个方向：更好支持微服务和容器（Scalable IOV)与适用于网络功能的上层协议（类比HTTP之于Web服务）
>
---


### 5.Self-driving networks
`Ming Zhang`-`Principal Engineer at Alibaba Group`-[[Slides]](https://conferences.sigcomm.org/events/apnet2018/slides/ming.pdf)

> `Xinchen Wan:`
> 
> * Alibaba’s self-driving networks is a very interesting and challenging topic. Traditionally, the whole network management life cycle is controlled by human. 
> * **Self-driving** networks aims at operating them in an automatic way and through the introduction, they settle fault detection and fault diagnosis by network itself successfully. <b> I suppose with the combination of AI technologies and network management, the large scale network can be smarter at routing strategies, auto-healing etc.</b>
>
>Tencent/Huawei smart NIC designs try to solve problems in general public cloud environments. <b>For us, we can focus on AI cluster setting, what are the best NIC functions we should provide in this customized context, what are the preferred properties the AI transport protocol should deliver, how to efficiently implement them in NIC hardware?</b> . I believe it will be much simpler and light-weighted than what described in their presentation. But that's something promising for us to pursue.
> 
---

> `Zhuoyi Peng:`
>
>Ming Zhang’s Self-driving networks enhances the conception of “Self-driving” from freeing the human work in network management, but his talk preserve many details and tricks that we should go deeper in. 
>
---

### 6.High perfomance Cloud with Hardware Acceleration
`Yong Ren`-`IaaS Chief Product Planning Expert in Huawei Could BU` -[[Slides]](https://conferences.sigcomm.org/events/apnet2018/slides/yong.pdf)


# SIGCOMM Talks
### 1. Elastic Sketch: Adaptive and Fast Network-wide Measurements
`Tong Yang`-`Research Assistant Professor at Peking University`-[[Slides]](https://conferences.sigcomm.org/events/apnet2018/slides/elasticsketch.pptx)

#### Brief Summary:

When network is undergoing problems such as congestion, scan attack, DDoS attack, etc., measurements are much more important than usual. In this case, traffic characteristics including available bandwidth, packet rate, and flow size distribution vary drastically, significantly degrading the performance of measurements. To address this issue,<b> we propose the Elastic sketch. It is adaptive to currently traffic characteristics.</b> Besides, it is generic to measurement tasks and platforms. We implement the Elastic sketch on six platforms: P4, FPGA, GPU, CPU, multi-core CPU, and OVS, to process six typical measurement tasks. Experimental results and theoretical analysis show that the Elastic sketch can adapt well to traffic characteristics. Compared to the state-of-the-art, the Elastic sketch achieves 44.6 ~ 45.2 times faster speed and 2.0 ~ 273.7 smaller error rate.

#### [[Paper Summary: miqianmimi ] ](https://github.com/miqianmimi/paper-notes/blob/master/18APNET/11st-08-2018.Elastic%20Sketch:Adapative%20and%20Fast%20Network.md)

---

###  2. AuTO: Scaling Deep Reinforcement Learning to Enable Datacenter-Scale Automatic Traffic Optimization
`Li Chen`-`Senior Software Engineer at Tencent`-[[Slides]](https://conferences.sigcomm.org/events/apnet2018/slides/auto.pptx)


#### Brief Summary:

And during the SIGCOMM talks, I’ve learnt a brief architecture of Li Chen’s AuTO optimization. AuTO is a two-level DRL system for datacenter-scale automatic traffic optimization which seperates flows in two parts: long flows and short flows by using MLFQ introduced in PIAS. It detached time-consuming DRL processing from quick action-taking for short flows. All end-hosts make instant TO decisions locally for short flows and the Central System makes individual TO decisions for long flows according to the global traffic information it collected. MLFQ schedules flows guided by a set of thresholds. The thresholds are set initially and then optimized by sRLA in the CS according to the global traffic over a relatively longer period of time. However I haven’t yet understand the details of MLFQ and DDPG, PG algorithms and it drives me to read AuTO source code to figure them out.

Before reading AuTO, you may want to read PIAS first. MLFQ is a nice approach you can leverage in more designs as you will see later.

Traffic optimizations (TO, e.g. flow scheduling, load balancing) in datacenters are difficult online decision-making problems. Previously, they are done with heuristics relying on operators’ understanding of the workload and environment. Designing and implementing proper TO algorithms thus take at least weeks. Encouraged by recent successes in applying deep reinforcement learning (DRL) techniques to solve complex online control problems, we study if DRL can be used for automatic TO without human-intervention.

However, our experiments show that the latency of current DRL systems cannot handle flow-level TO at the scale of current datacenters, because short flows (which constitute the majority of traffic) are usually gone before decisions can be made. 

Leveraging the long-tail distribution of datacenter traffic, we develop a two-level DRL system, AuTO, mimicking the Peripheral & Central Nervous Systems in animals, to solve the scalability problem. Peripheral Systems (PS) reside on end-hosts, collect flow information, and make TO decisions locally with minimal delay for short flows. PS’s decisions are informed by a Central System (CS), where global traffic information is aggregated and processed. CS further makes individual TO decisions for long flows. With CS&PS, `AuTO` is an end-to-end automatic TO system that can collect network information, learn from past decisions, and perform actions to achieve operator-defined goals. We implement AuTO with popular machine learning frameworks and commodity servers, and deploy it on a 32-server testbed.

Compared to existing approaches, AuTO reduces the TO turn-around time from weeks to ~100 milliseconds while achieving superior performance. For example, it demonstrates up to 48.14% reduction in average flow completion time (FCT) over existing solutions.

#### [ [Paper Summary: miqianmimi ] ](https://github.com/miqianmimi/paper-notes/blob/master/18APNET/11st-08-18%20AuTO:Scaling%20Deep%20Reinforcement%20Learning.md)

---

> `Xinchen Wan:`
> 
> I’ve learnt a brief architecture of Li Chen’s AuTO optimization. 
> 
> AuTO is a two-level DRL system for datacenter-scale automatic traffic optimization which seperates flows in two parts: long flows and short flows by using MLFQ introduced in PIAS. 
> 
> It detached time-consuming DRL processing from quick action-taking for short flows. <b>All end-hosts make instant TO decisions locally for short flows and the Central System makes individual TO decisions for long flows according to the global traffic information it collected.</b>
> 
> MLFQ schedules flows guided by a set of thresholds. The thresholds are set initially and then optimized by sRLA in the CS according to the global traffic over a relatively longer period of time. <b> However I haven’t yet understand the details of MLFQ and DDPG, PG algorithms and  it drives me to read AuTO source code to figure them out.</b>

> <b>Before reading AuTO, you may want to read `PIAS` first. `MLFQ` is a nice approach you can leverage in more designs as you will see later.</b>
> 
---
> 
>  `Duowen Liu:`
>  
>  This is a sigcomm paper talk by Li Chen,In this paper he focused on `Traffic Optimization(TO)` problems in data centers and tried to use `Deep Reinforcement learning(DRL)` techniques to solve them.
>  
>  However, The experiment shows that DRL systems now have too long latency to deal with short flows which are usually gone before decision is made.
>  
>  They developed a Peripheral System(PS) to collect information from short flows and make decisions with minimal delay locally Central System(CS) will aggregate and process global traffic information and make TO for long flows
>  
 ---
>  
> `Zhuoyi Peng:`
>  However, Li Chen’s work make real breakthrough in combining AI and traditional network problem. 
>   
>  He uses reinforcement Learning to replace heuristics solution in traffic optimization. The two-level DRL system, `AuTO`, efficiently achieves a great balance between flow-level TO and DRL decision making. 
>   
>  For further discussion, other combinations in AI algorithm and network problem which AI algorithm applies attract me a lot(e.g more robust model and actual data-intensive network problem that provides enough data for feeding). I think we can implement more AI-Networking combination with real world impact indeed.
> 
 ---

> `Yuchao Zhang:`
> Tencent 的 Li Chen聚焦datacenter-scale 的Traffic Optimization(TO, e.g. flow scheduling, load balacning)问题， 做了基于深度学习的自动流量优化工作，这里的challenge是time-consuming DRL processing vs quick action-taking.为了避免小流量在决策之前就已经gone, 作者设计了巧妙地Peripheral Systems(PS)+ Central System(CS)的解决方案。
>
> ---

### 3. SketchLearn: Relieving User Burdens in Approximate Measurement with Automated Statistical Inference
`Qun Huang`-`Associate Professor at ICT, CAS]`-[[Slides]](https://conferences.sigcomm.org/events/apnet2018/slides/sketchlearn.pptx)

#### Abstract:

 Network measurement is challenged to fulfill stringent resource requirements in the face of massive network traffic. While approximate measurement can trade accuracy for resource savings, (近似估计可以丧失一点准确性) it demands intensive manual efforts to configure the right resource-accuracy trade-offs in real deployment. 

 Such user burdens are caused by how existing approximate measurement approaches inherently deal with resource conflicts when tracking massive network traffic with limited resources. In particular, they tightly couple resource configurations with accuracy parameters, so as to provision sufficient resources to bound the measurement errors.(特别是，它们将资源配置与精度参数紧密耦合，以便提供足够的资源来约束测量误差。) 

 <b> We design SketchLearn, a novel sketch-based measurement framework that resolves resource conflicts by learning their statistical properties to eliminate conflicting traffic components.</b> (解决资源冲突，通过学习统计特性)We prototype SketchLearn on OpenVSwitch and P4, and our testbed experiments and stress-test simulation show that SketchLearn accurately and automatically monitors various traffic statistics and effectively supports network-wide measurement with limited resources.

#### [ [Paper Summary: miqianmimi ] ](https://github.com/miqianmimi/paper-notes/blob/master/18APNET/13rd-08-18%20SketchLearn-%20Relieving%20User%20Burdens%20in%20Approximate%20Measurement%20with%20Automated%20Statistical%20Inference.md)

----

### 4. PLoRa: A Passive Long-Range Data Network from Ambient LoRa Transmissions
`Yao Peng`-`Associate Professor at Northwest University, China`-[[Slides]](https://conferences.sigcomm.org/events/apnet2018/slides/plora.pptx)

#### Breif Summary:

The next-generation Internet of Things (IoT) envisions ubiquitous, cheap, and low data-rate connectivity among humans, machines, and objects, 

for example, a farmer could remotely monitor nutrition levels in a field; a biologist could keep track of wild animal movement, group formulation and population demographics.

A key to this vision is the wireless communication technology that enables extremely impoverished IoT devices to continuously exchange low-rate data. Ideally, such wireless communication should satisfy the following three `requirements`: **battery-free, long-range and ambient excitation signal**.Realizing these visions require addressing three significant `challenges`: **proper packet detection, modulation and tightly power constraints.** 

* First, since the tag is battery-free, it should consume an ultra-low amount of power during which it is idle, listening to detect an incoming ambient information packet. 

* Second, as the excitation signal that conveys data and change over time, it is thus challenging to modulate this time-varying excitation signal into another standard ambient signal for backscatter. 

* Third, given the large energy demands of the computational and communication tasks, the battery-free tag will soon drain its energy and stop working, which will cause complete loss of data stored in its volatile memory. 

In this talk, I will present `PLoRa`, an ambient backscatter design that enables long-range wireless connectivity for battery-less IoT devices. Our experimental results demonstrate that our prototype PCB PLoRa tag can backscatter an ambient LoRa transmission sent from a nearby LoRa node to a gateway up to 1.1 km away, and deliver 284 bytes data every 24 minutes indoors, or every 17 minutes outdoors.

#### [ [Paper Summary: miqianmimi ] ](https://github.com/miqianmimi/paper-notes/blob/master/18APNET/13rd-08-18%20PLoRa-%20A%20Passive%20Long-Range%20Data%20Network%20from%20Ambient%20LoRa%20Transmissions.md)

----

### 5. A Measurement Study on Multi-path TCP with Multiple Cellular Carriers on High Speed Rails
`Tong Li`- `Senior Researcher in 2012 Labs of Huawei`-[[Slides]](https://conferences.sigcomm.org/events/apnet2018/slides/hsr-mptcp.pdf)

#### Breif Summary:

Recent advances in high speed rails (HSRs) are propelling the need for acceptable network service in high speed mobility environments. However, previous studies show that the performance of **traditional single-path transmission** degrades significantly during high speed mobility due to frequent handoff. 

**Multi-path transmission** with multiple carriers is a promising way to enhance performance, because at any time, there is possibly **at least one path not suffering a handoff**. 

In this paper, for the first time, we measure `multi-path TCP (MPTCP)` with two cellular carriers on HSRs with a peak speed of 310km/h. We find a significant difference in handoff time between the two carriers.

Moreover, we observe that `MPTCP` can provide much better performance than TCP in the poorer of the two paths. This indicates that **MPTCP’s robustness to handoff is much higher than TCP’s.**

> However

The efficiency of MPTCP is far from satisfactory.**MPTCP performs worse than TCP in the better path most of the time.**

The low efficiency can be attributed to poor adaptability to frequent handoff by MPTCP’s key operations in sub-flow establishment, congestion control and scheduling. Finally, we discuss possible directions for improving MPTCP for such scenarios.

#### [ [Paper Summary: miqianmimi ] ](https://github.com/miqianmimi/paper-notes/blob/master/18APNET/13RD-08-18%20A%20Measurement%20Study%20on%20Multi-path%20TCP%20with%20Multiple%20Cellular%20Carriers%20on%20High%20Speed%20Rails.md)

---

>`Zhuoyi Peng:`
>
>Tong Li’s work made insight into the protocol part and all of them are worth appreciation.

---

# Other papers and thought:
### 1.Toward Effective and Fair RDMA Resource Sharing 
`Haonan Qiu`-[[Slides]](https://conferences.sigcomm.org/events/apnet2018/slides/avator.pptx)

> `YuNan Zhang:`
> 这篇是来自南京大学的Best Paper，针对RDMA场景下Queue Pair对资源利用的情况，指出Strict priority 和 Enhanced Transmission Selection 都不能再multi-application情况下公共共享机器资源，提出了Avatar的解决方案，在Connection establishment, Traffic Scheduling, Traffic receiving 三个环节实现了细粒度的调度

### 2.`Panel 1` Network Infrastructure for Next Generation Cloud
`Kun Tan`- `Huawei`

>  `Bojie Li:`
>  
>  1.网络的调试和诊断仍然很重要，尤其是没有代码的黑盒情况下，在一个自动运维的网络中，需要有故障检测，故障诊断和预测，故障恢复几个部分。需要AI技术来预测应用需求，做好网络容量规划，预测网络故障，分析故障的根本原因。
> 
>  2.从虚拟机到容器、微服务、无服务器计算、云计算的力度越来越细，这对端到端延迟提出了高要求。一方面，网络的多个层次（如三层，四层，应用层协议）需要融合，提出端到端的通信解决方案。另一方面，SmartNIC,可编程交换机将进一步部署，以提高性能和调试能力，其中CPU和可变成硬件之间的接口（ISA)需要更多思考，此外，In-network computing 也带来了网络和系统融合的机遇。
>  
>  3.网络领域没有基础的重大挑战，但是有几个趋势：首先，目前Internet的连接方式是云+端，过去十年主要变化是从云到端经过的ISP数量更少了，WAN优化成为可能；未来十年也会有很大的位置变化。其次，数据中心网络带宽的增长尽管近年来超过摩尔定律，未来也会受到摩尔定律的影响放缓。最后，网络安全愈加重要，复杂的理论方案在生产环境未必合适，量子计算是个早期单有前途的方向。
>  
>  4.以AR/VR和自动驾驶为代表的AI应用需要把AI计算能力部署到边缘(edge).一方面，边缘设备的资源数量有限，与云端架构明显不同。另一方面，边缘上的计算设备是异构的。网络作为互联异构设备的基础设施，需要更多智能。
>  
>  5.对发表论文的建议：不要发表least publishable unit，研究的目的是找到一个问题的靠谱解决方案，而非文章越早发表，数量越多越好。研究相比工程最大的好处是奢侈的自由。
>  
>  6.P4 和可变成网络引发了热烈讨论，P4把网络可编程性变成了热点，可变成网络当然是有用的网络新视角，但它是手段而非目的。特别地，P4是不是正确的抽象，是不是一个成熟到可以大规模部署的抽象，他显然不是一个完备的抽象，也不应该是唯一的抽象，正如编程语言有ISA、字节码、C、Python等不同的层次。做网络编程研究的时候不能只考虑有趣，而是从用户和商业的角度考虑：一方面需要把实际应用的成本降低0.2-0.5，另一方面是需要在性能上实现低延迟，高带宽。
>  
 ---

>  `Xinchen Wan:`
>  
>  What impressed me most was the experts’opinions about the comparison between P4 chips ‘Tofino’ and Broadcom chips. As we know, P4 is a high-level language for programming packet processors. It is useful for engineers to customize their network processing strategies as they want, which gives us flexibilities. The experts didn’t give a direct conclusion about the comparison to us because they seem haven’t yet test the network performances with those two chips.
>  
>  However, by listening to their answers, programable network seems to have a promising future for research and productive environment. And the best way to figure out which counts more is from the customers’ perspective or the companies’. That is, if you have a fewer cost and better performances(low latency and better advantages to the network), then people are happyier to deploy it.

> P4 is a bit far from production deployment for now. Let's keep an eye on it. For now, I think we can program at the edge, i.e., NIC, instead of jumping into programming switches.
>
---
 
> `Zhuoyi Peng:`
>
> The panel part observes the brain storm of the advanced researchers and engineers and among such interesting questions, I determine to explore more in networking support for Cloud, Big-Data, and AI Systems.
> 
---

> `Yuchao Zhang:`
> 
> 网络从传统的服务器-客户端的模式，成功演化成了DCN as backend--CDN as frontend的模式，也逐步体现出了AI Cloud -- endhost的趋势，其中AI cloud 来做智能决策，整个网络自动运行，自动维护，AI improves network and network accelerates AI, 相辅相成，共同演进。
> 
> `Promising Topics:`
> * Lossy RDMA on > 100G link
> * Access control/Scheduling (Macroflow)
> * Offloading: endhost vs Cloud server
> * Programmable hardware
> * AI Cloud Management
> * ML alogrithm with network
>
---

### 3.System Acceleration - Macroflow
`Bingchuan Tian`-[[Slides]](https://conferences.sigcomm.org/events/apnet2018/slides/macroflow.pptx)

> `Yuchao Zhang:`
> 
> 对System Acceleration方向的文章感兴趣，包括ML算法的Parallel Model.
> 
> 第一篇来自南京大学,针对Hadoop场景下machine slot-time的调度，作者指出flow level和co-flow level 都不足以最小化Job的完成时间。因此提出了Macroflow的概念。即an abstraction with a granularity between flow and coflow,设计了 Smallest Macroflow First(SMF) 和Smallest-Average-Macroflow-First(SAMF)算法来做调度优化。归类为Scheduling.
> 
 ---

### 4.System Acceleration - GEN
`Zhilong Zheng`-[[Slides]](https://conferences.sigcomm.org/events/apnet2018/slides/gen.pptx)

> `Yuchao Zhang:`
>  
> 这一篇来自清华大学,指出现在的NFV都是CPU-based，pipeline-based,在 high-performance 和 high elasticity 的方面都差强人意。
> 
> 因此提出了GPU的NFV实现方案，两个主要的Components,orchestrator is responsible for SFC construction and modifiation, while the controller steers packets among NFs.
>
 ---
