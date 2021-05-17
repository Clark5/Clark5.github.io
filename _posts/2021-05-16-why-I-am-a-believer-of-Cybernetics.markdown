---
layout:     post
title:      "Why I am a believer of Engineering Cybernetics"
subtitle:   ""
date:       2021-05-16 
author:     "Weitao Wang"
header-img: "img/post-bg-os-metro.jpg"
catalog: true
tags:
    - Research Mottos
    - Engineering Cybernetics
---

> "The purpose of "Engineering Cybernetics" is then to study those parts of the broad science of cybernetics which have direct engineering applications in designing controlled or guided systems. It certainly includes such topics usually treated in books on servomechanisms. But a wider range of topics is only one difference between engineering cybernetics and servomechanisms engineering. A deeper - and thus more important - difference lies in the fact that engineering cybernetics is an engineering science, while servomechanisms engineering is an engineering practice." --- Xuesen Qian

This is my first post, and I will briefly introduced some of my research mottos learned from Cybernetics and Engineering Cybernetics: science (math) matters, abstraction is the bridge, probabilistic is the key observation, and feedback is always required in any engineering practice.

### Engineering Science V.S. Engineering Practice

The first thing I want to discuss is that the importance of science in engineering problems.

Long time ago, the engineering is considered as a practical subject driven by try-and-error. People invent steam engines but have no idea why boiling water could transfer the force through a crank arm connecting rod and make the sewing machine spin, but they know this machine works fine if you carefully control the heat under that boiler. Moreover, they also kept in mind the interval to throw coals under a boiler. When the sewing machine is too fast, just delay the coal, and when it is too slow, the coal stove worker may be asked to work harder.

People knows a lot about the practice and summarize the experience from the daily try-and-error, but the real technology takes off when the quantitative science, like math, probability theory, and thermodynamics, are introduced to engineering. Nowadays, people can launch a extremely complex manned spacecraft to the Space successfully at the first time, which should credits to the cybernetic science. **The only thing that always holds true is the science behind every machine or system.**

### Probability Is The Key When Using The Theory

But sometimes the theory does not work as you expected, it is not because the theory are wrong, instead, it is the input of the system that should be blame for. One of the laws of nature is that the the observations are always random variables with a mean and a variance. This variance partly comes from the nature of the object that we are observing, and partly comes from the observation process itself. 

You can measure the length of 10 pens aside the assembly line to infer the average of one million pens that was made by this assembly line, but you cannot do the same thing to infer the average human heights in a district. Similarly, when you measure the length of pens, you will tend to have similar measurements using a vernier caliper rather than using the palm of your hand.

In this case, your system need to handle the all the inputs that locate insides the valid probabilistic range. **Not only be aware of the probabilities, the systems should be designed based on the observation on the inputs' randomness.**

### Feedback Loop Is Always Required

However, nature always wants to surprise us and hold the Murphy's Law as its sword. Even if some situations are very unlikely to happen, it will happens if your system runs long enough.

Nuclear power plants are one of the safest factory and every operations requires double checks. Even in this case, people will still have tons of emergency plans in cases something unexpected happens. And it does happen and even out of the scope of emergency plans. I used to love Salmon. :-(

**As a engineer, we all should respect the randomness and take every situation into consideration, even for those unlikely situations.** A feedback loop is always required in a robust system. Only in this way, the system can be kept in the favorable scope and will not crash when the extreme case happens.

### BTW, Fill The Gap Between Science And Engineering

Though, there is still a gap between science and the engineering: what theory should we use, and why it is the best science theory that we should refer to?

There are a lot of science theories in this world. Some of them are fundamental like Newton's three laws and Maxwell's equations, others are inferences based on the fundamental theories. Clearly as a engineer, it is not our job to derive from the fundamental theories and get the correct inference theory for our problem. In most cases, even those best engineers are referring to the existing **well-known** math problems and theories when they looking for theoretical support based on the analogy between the engineering problem and the existing problems. And the key behind the analogy is the abstraction.

By abstracting the problems, you will get a simple, native, and mathematical description of the problems. After that, it would be much easier for you to find out the relevant theoretical supports.

Another benefit is that, with abstraction, you could solve similar engineering problems in the near future. Based on my knowledge, the specific engineering subject always related to a group of science fields. For example, the task scheduling highly relies on queuing theory, the data center network is built on top of the graph theory, and the machine learning is also a practice of Bayes' theorem.

Last but not the least, abstraction is significant when you call for help. Our current society is highly developed with highly specialized division of labor, it is no longer encouraged to work on your own. Mathematicians, physicists, and materials scientists should work together with engineers before designing a spaceship. **It is much easier for you, the engineers, to provide an abstracted problems to those scientist, rather than require a 76-years-old mathematicians to learn circuit design by himself.**

### Conclusion

I don't stand for every theory in Cybernetics or Engineering Cybernetics, it is the scientific spirit to narrow every problem into math and probability that attract me all the time.
