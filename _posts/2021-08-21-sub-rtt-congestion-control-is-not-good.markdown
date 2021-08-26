---
layout:     post
title:      "Why is Sub-RTT Congestion Control NOT Good?"
subtitle:   ""
date:       2021-08-21
author:     "Weitao Wang"
header-img: "img/about-bg-walle.jpg"
catalog: true
tags:
    - Network
    - Congestion Control
    - Research
---

Tl;DR: The fluid model allocates the bandwidth based on the most congested hop, sub-RTT CC usually didn't get the congestion information from all the hops (otherwise, it will just become RTT), so that they don't have the enough information to make the perfect response to the congestion. The sub-RTT can be used as compliment for a normal RTT-based CC, but it usually cannot be used as the standalone CC protocol.
