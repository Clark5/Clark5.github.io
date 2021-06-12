---
layout:     post
title:      "Why I am a believer of Engineering Cybernetics"
subtitle:   ""
date:       2021-05-16 
author:     "Weitao Wang"
header-img: "img/post-bg-os-metro.jpg"
catalog: true
tags:
    - Mottos
    - Cybernetics
---

> "The purpose of "Engineering Cybernetics" is then to study those parts of the broad science of cybernetics that have direct engineering applications in designing controlled or guided systems. It certainly includes such topics usually treated in books on servomechanisms. But a wider range of topics is only one difference between engineering cybernetics and servomechanisms engineering. A deeper - and thus more important - difference lies in the fact that engineering cybernetics is an engineering science, while servomechanisms engineering is an engineering practice." --- Xuesen Qian

This is my first post, in which I will briefly introduce some of my research mottos learned from Cybernetics and Engineering Cybernetics: science (math) matters, probabilistic is the key observation, feedbacks are required in any engineering practice, and abstraction is the bridge between engineering and science.

### Engineering Science V.S. Engineering Practice

The first thing I want to discuss is the importance of science in engineering problems.

A long time ago, engineering is considered to be a practical subject driven by try-and-error. In 1700s, people invented steam engines but have no idea why boiling water could transfer the force through a crank arm connecting rod and make the sewing machine spin, but they know this machine works fine if you carefully control the heat under that boiler. Moreover, they also kept in mind the speed to throw coals under a boiler. When the sewing machine runs too fast, the worker will just delay the coal, and when it is too slow, the coal stove worker may be asked to work harder.

People knows a lot about the practice and summarize the experience from the daily try-and-error, but the technology takes off when the quantitative science, like math, probability theory, and thermodynamics, are introduced to engineering (the theory of steam engine, Carnot cycle, is found in 1824). Nowadays, people can launch a extremely complex manned spacecraft to the Space successfully at the first time without try-and-error, which should credit to the science of cybernetic. **Systems cannot last forever, the only thing that always holds true is the science behind every machine or system.**

### Probability Is The Key When Using The Theory

But sometimes the theory does not work as you expected, it is not because the theory are wrong, instead, it is the input of the system that should be blame for. One of the laws of nature is that the observations are always random variables with a mean and a variance. This variance partly comes from the nature of the object that we are observing, and partly comes from the observation process itself.

For instance, you can measure the length of 10 pens aside a assembly line to infer the average of one million pens that was made by this assembly line, but measuring 10 random people is far from enough to infer the average human heights in a district. Similarly, when you measure the length of pens, you will tend to have better accuracy when using a vernier caliper rather than using the palm of your hand for estimation.

So that, your system need to handle the all the inputs that locate insides the valid probabilistic range. **Not only be aware of the probabilities, the systems should be designed based on the observation on the inputs' randomness.**

### Feedback Loop Is Always Required

Even if we build our system on top of a reasonable probabilistic range, however, nature always wants to surprise us and hold the Murphy's Law as its sword. Even if some situations are very unlikely to happen, it will happens if your system runs long enough.

Nuclear power plants are one of the safest factory and every operations requires more than double checks. Even in this case, people will still have tons of emergency plans in cases something unexpected happens. And those unexpected events did happen and even out of the scope of emergency plans, like what happened in Chernobili and Fukushima.

**As a engineer, we all should respect the randomness and take every situation into consideration, even for those unlikely situations.** A feedback loop is always required in a robust system. Only in this way, the system can be kept in the favorable scope and will not crash when the extreme case happens.

### BTW, Fill The Gap Between Science And Engineering

Finally, there is still a gap between science and the engineering: what theory should we use, and why it is the best theory that we should refer to?

There are a lot of science theories in this world. Some of them are fundamental like Newton's three laws and Maxwell's equations, others are inferences based on the fundamental theories. Clearly, as a engineer, it is not our job to derive from the fundamental theories and get the correct inference theory for our problem. In most cases, even those best engineers are referring to the existing **well-known** math problems and theories when they looking for theoretical supports. To find such analogy between the engineering problem and the existing problems, the key skill is the abstraction.

By abstracting the problems, you will get a simple, native, and mathematical description of the problems. After that, it would be much easier for you to find out the relevant theoretical supports.

Another benefit is that, with abstraction, you could solve similar engineering problems in the near future. Based on my knowledge, a specific engineering subject is usually related to a certain group of science fields. For example, the task scheduling highly relies on queuing theory, the data center network is built on top of the graph theory, and the machine learning is also a practice of Bayes' theorem.

Last but not the least, abstraction is significant when you call for help. Our current society is highly developed with highly specialized division of labor, it is no longer encouraged to work on your own. Mathematicians, physicists, materials scientists, etc, should work together with engineers before designing any complex engineering systems. **It is much easier for you, the engineers, to provide an abstracted problem to those scientist, rather than require a 76-years-old mathematicians to learn circuit design by himself.**

### Conclusion

I don't stand for every theory in Cybernetics or Engineering Cybernetics, it is the thoughts to narrow every problem into math and probability that attract me all the time.
