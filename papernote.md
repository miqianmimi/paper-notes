# paper note

## 1.[RDMA over Commodity Ethernet at Scale](http://delivery.acm.org/10.1145/2940000/2934908/p202-guo.pdf?ip=175.159.126.197&id=2934908&acc=PUBLIC&key=CDD1E79C27AC4E65%2EFC30B8D6EF32B758%2E4D4702B0C3E38B35%2E4D4702B0C3E38B35&__acm__=1526398003_b29114454296136b27e611a692059607)
* [ Slice ](https://conferences.sigcomm.org/events/apnet2017/slides/cx.pdf)
### 3 things I understand quickly:
* Why DC choose RDMA: 
low latency, low CPU overhead, high throughput
* What difficulty RDMA faces:
PFC-induced deadlock, RDMA transport livelock, NIC PFC pause frame storm problem
* The conclusion of the RDMA problem solving:
Only running RoCEv2 **at scale for intra-dc network** RDMA can in this way completly replace of TCP/IP in dc.
