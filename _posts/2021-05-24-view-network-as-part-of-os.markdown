---
layout:     post
title:      "View network as a part of the operating system"
subtitle:   ""
date:       2021-05-24
author:     "Weitao Wang"
header-img: "img/post-bg-datacenter-network.jpg"
catalog: true
tags:
    - Network
    - Research
---

# View network as a part of the OS

Nowadays, the latency requirement and the throughput desire on the data center network keep increasing, along with the new technologies like NVMe, Optane memory, in-memory file system, and disaggregated data centers. The bottleneck of the services is shifting from the host-side CPU/GPU computation to the network transmission, and one indication is that the over-subscribed network is replaced by the non-blocking network in most data centers.

To solve this problem, industries as well as academias all accepted that the network should be viewed as an I/O of the operating systems and a latency-target should be given along with the transmission tasks to the network stack. However, is it really a good choice to leave the network transmissions unattended and accept the possibility of SLO violations?

The benefit from this new view has been explained in one of my paper: [MXDAG: A Hybrid Abstraction for Cluster Applications](https://arxiv.org/abs/2107.07442).