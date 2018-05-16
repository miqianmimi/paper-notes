# paper note

### 1.[RDMA over Commodity Ethernet at Scale](http://delivery.acm.org/10.1145/2940000/2934908/p202-guo.pdf?ip=175.159.126.197&id=2934908&acc=PUBLIC&key=CDD1E79C27AC4E65%2EFC30B8D6EF32B758%2E4D4702B0C3E38B35%2E4D4702B0C3E38B35&__acm__=1526398003_b29114454296136b27e611a692059607)
* [ Slice ](https://conferences.sigcomm.org/events/apnet2017/slides/cx.pdf)
### 3 things I understand quickly:
* Why DC choose RDMA: 
low latency, low CPU overhead, high throughput
* What difficulty RDMA faces:
PFC-induced deadlock, RDMA transport livelock, NIC PFC pause frame storm problem
* The conclusion of the RDMA problem solving:
Only running RoCEv2 **at scale for intra-dc network** RDMA can in this way completly replace of TCP/IP in dc.
[✅Stanford NetSight1](http://www.scs.stanford.edu/~dm/home/papers/handigol:netsight.pdf)
[✅Stanford NetSight2](http://yuba.stanford.edu/~nickm/papers/nikhil-thesis.pdf)
[✅Microsoft Pingmesh](https://www.microsoft.com/en-us/research/publication/pingmesh-large-scale-system-data-center-network-latency-measurement-analysis/)
[✅RDMA VS TCP](https://www.youtube.com/watch?v=u5EWqojkI1A)
[✅DC needs RDMA](https://conferences.sigcomm.org/events/apnet2017/slides/cx.pdf)
[✅RDMA over Ethernet中文版](https://blog.csdn.net/upupday19/article/details/79219897)
[✅RDMA PFC死锁 RDMA活锁 郭传雄草稿](http://blog.sina.com.cn/s/blog_569dd33a0102wzg4.html)
[✅ 吞吐与延迟](http://www.cnblogs.com/binyao/p/5162424.html)
[✅RDMA no need of lossless](http://netseminar.stanford.edu/seminars/03_16_17.pdf)
[✅RDMA 的性能异常](http://www.mosharaf.com/wp-content/uploads/fairdma-kbnets2017.pdf)
* Realize that 我并不应该先去找缺点，然后再从实验中验证缺点，因为我的实验器材中没有ToR,NIC,而且上述的缺点都是偶然概率事件，因此我应该先得出rping实验数据,作出图后，根据图再进行分析。
