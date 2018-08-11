# Elastic Sketch:Adapative and Fast Network-Wide Measurements
* [TongYang] 
* [Keywords: Network measurement]

## Abstract

> ### 1.contribution
> Network is undergoing problems such as congestion, scan attack.
traffic characteristics including bandwidth packet rate, and flow size distribution vary drastically, which result in bad measurement.

> * To address this issue, we propose the Elastic sketch.
> * Implement this on six platforms: P4, FPGA, GPU, CPU, multi-core CPU and OVS
> * 44.6 ~ 45.2 times faster speed and 2.0 ~ 273.7 smaller error rate.

> ### 2.related work
> The state-of-the-art UnivMon makes a good trade-off among these four dimensions.

> But they do not focus on one fundamental need: achieving accurate network measurements no matter how traffic characteristics(available bandwidth, flow size distribution, and packet rate)vary.

## Introduction

* first characteristic : available bandwidth

* second characteristic : packet arrival rate

* third characteristic : flow size distribution

> It is desirable to design an elastic data structure which can dynamically allocate appropriate memory size for elephant flows.

> Requrie our sketch to be elastic: adaptive to bandwidth, packet rate and flow size distribution. Besides, three other requriements in measurements:
generic, fast and accurate.

## How
<b>the Elastic Sketch has two parts: a heavy part and a light part.</b>

<b>Ostracism : a separation technique to keep elephant flows in the heavy part , and mouse flows in the light part. </b>

### make it "elastic", we do the following:

> * (1) to be adpative to bandwidth.
we propose algorithms to compress and merge sketches.
we use servers to merge sketches and reduce the bandwidth usage.

> * (2) packet rate high , change the processing method. each packet only accesses the heavy part to record the information of elephant flows exclusively.discarding the information of moue flows.

> * (3) As the number of elephant flows varies and is unknown in advance, we propose an algorithm to dynamically increase the memory size of the heavy part.

### make "generic", we do the following:

> * (1) to be generic in terms of measruement tasks

> * (2) To be generic in terms of platforms

> tailor a P4 version of the Elastic sketch, given the popularity of this platforms.




