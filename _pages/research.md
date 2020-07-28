---
layout: page
title: Research
permalink: /res/
<!-- image: images/back.jpeg -->
---

## Formal Analysis of Cyber-physical Systems

> Formally modelling and verifying a complex CPS is extremely challenging, can we automatically learn for verifying such systems without manual modelling?

### Series of Works
- [[ETAPS/FASE 2017, STTT 2018](http://158.64.76.181/bitstream/10993/36876/1/STTT18.pdf)] Conducted an empirical study on learning probabilistic models (e.g., discrete-time Markov Chains) from system traces, and proposed a new learning framework based on genetic algorithms.
- [[TSE 2018](https://ieeexplore.ieee.org/abstract/document/8576657/)] Proposed a CEGAR-style predicate abstraction-based learning framework to push forward learning to be applicable for large-scale systems with even infinite state space.
- [[ICFEM 2017](https://ink.library.smu.edu.sg/cgi/viewcontent.cgi?article=5711&context=sis_research)] Proposed an active learning algorithm to sample the system so that a more acurate model can be learned.
- [[FM 2018](https://arxiv.org/pdf/1712.04155.pdf)] Conducted a case study of the above learning algorithms on the verification of a real-world testbed, i.e., [SWaT](https://itrust.sutd.edu.sg/testbeds/secure-water-treatment-swat/).
- [[DSN 2018](https://ink.library.smu.edu.sg/cgi/viewcontent.cgi?article=5970&context=sis_research)] Proposed an importance sampling algorithm of the learned approximate probabilistic model to obtain a more accurate verification result where rare events are potentially involved.
- [[ICSE 2018](https://ink.library.smu.edu.sg/cgi/viewcontent.cgi?article=5655&context=sis_research), <font color="#dd0000">ACM SIGSOFT Distinguished Paper Award</font>] Applied the idea of probabilistic learning to model program concolic testing, solved the optimal strategy and proposed a greedy algorithm to approximate the strategy. 

## Software Engineering for Dependable Artificial Intelligence Systems

> AI is deeply interwined with software engineering. While AI systems can be intrinsically vulnerable/discriminative to be trusted, software engineering could help either by testing or formal verification.


### Series of Works
- [[ICSE 2019](https://arxiv.org/pdf/1812.05793.pdf)] Proposed a runtime detection system framework to filter adversarial samples of deep neural networks. Compared to prior detection algorithms, it is sufficiently efficient to be applicable at runtime.
- [[ICSE 2020](https://ink.library.smu.edu.sg/cgi/viewcontent.cgi?article=5635&context=sis_research), <font color="#dd0000">ACM SIGSOFT Distinguished Paper Award</font>] Proposed a scalable and efficient algorithm which utilized gradient to search for disciminative samples of deep neural networks, which could be used for data augmentation to improve the model fairness.
- Several other works are in submission.