---
layout:     post
title:      "Can We Achieve Zero Queuing, Full Utilization, and Fast Convergence Simutaneously?"
subtitle:   ""
date:       2023-08-23
author:     "Weitao Wang"
header-img: "img/post-bg-js-module.jpg"
catalog: true
tags:
    - Network
    - Congestion Control
    - Research
---

Tl;DR: Any distributed congestion control algorithm is not able to achieve zero queuing, full utilization, and fast convergence to fairness at the same time. The inherent reason is that any congestion signal is consist of either utilization or queuing, in order to converge to fairness, the signal cannot always be zero queuing and full utilization all the time. 

### What are distributed congestion control algorithms?

The congestion control algorithms that only receive feedback from the aggregated traffic characteristic (e.g. latency, packet loss), but control the sending behavior of each individual flow on the sender side.

### LUC Theorem 

For the above-defined distributed CC algorithms, we argue a fundamental trade-off among the following three goals: For any distributed congestion control algorithm, at most 2 out of the 3 goals can be achieved: zero queuing latency (L), full utilization (U), and convergence (C).

The above theorem is based on the fact that the distributed CC algorithms are only allowed to use signals from the aggregated traffic. The intuition is that: (1) Under "LU", specifically 100\% bandwidth utilization without any queuing, distributed CC algorithms will not notice any signal changes, and consequently, each individual flow will not perform any update. (2) Under "LC", the aggregated throughput must change to give meaningful feedback. Assuming the maximum aggregated throughput is 100\% of the bandwidth, the lower aggregated throughput will under-utilize the link. (3) Under "UC", zero queuing latency cannot be achieved for a similar reason as "LC".

### A simple proof of LUC Theorem

Denote:
- $L_t$: The latency signal received by the CC algorithm to describe the aggregated traffic at time $t$;
- $U_t$: The utilization signal received by the CC algorithm to describe the aggregated traffic at time $t$;
- $S_t=Signal(L_t, U_t)$: the actual signal used by the CC algorithm, which is calculated based on the latency and utilization signals. Because latency and utilization are only two characteristics that can be used to describe aggregated traffic. We exclude the packet loss signal because we assume that packet loss is not allowed. 
- $R_t^f$: The rate for flow $f$ at time $t$;
- $Update(Signal, R)$: The update function for the CC algorithm, returns the rate update ratio;
- $B$: the link bandwidth;

Without loss of generality, we focus on congestion on only 1 hop to prove that zero-queuing latency, full utilization, and fast convergence cannot be achieved at the same time.

In the following, we will use contradiction to prove the LUC Theorem: Assume a CC could achieve zero-linking latency, fast convergence, and full utilization at the same time.

From the assumption, we can have:

$$U_t = U_{t'}, \forall t, t'$$

$$L_t = L_{t'}, \forall t, t'$$

Because the signal used by the CC algorithm is calculated based on the above 2 inputs, thus we can have:

$$S_t = Signal(L_t, U_t) = S(L_{t'}, U_{t'}) = S_{t'}$$

The signal for the CC algorithm never changes over time, so we also have (assuming there is no randomness in the update function):

$$Update(S_t, R) = Update(S_{t'}, R)$$

We also have:

$$R_{t+1}^f = R_t^f \cdot Update(S_t, R_t^f)$$

In the final state, the rate will never change. 

$$R_{t+1}^f = R_t^f$$

Combine the above equation, we can know:

$$Update(S_t, R_t^f) = 1.0, \forall R_t^f, \forall S_t$$

However, if the update ratio is always 1.0, convergence will not be achieved. Thus, by contradiction, we proved the LUC Theorem.
