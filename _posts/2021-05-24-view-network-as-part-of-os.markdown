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

Nowadays, the latency requirement and the throughput desire on the network keep increasing, along with the new technologies like NVMe, Optane memory, in-memory file system, and disaggregated data centers. The bottleneck of the services is shifting from the host-side CPU/GPU computation to the network transmission.

Nowadays, industries as well as academias all accepted that the network should be viewed as an I/O of the operating systems and a latency-target should be given along with the transmission tasks to the network stack. However, is it really a good choice to leave the network transmissions to be unattended and accept the possibility of SLO violations?

To be continued...