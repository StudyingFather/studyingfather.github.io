---
title: "Tunneling through the Hill: Multi-way Intersection for Version-Space Algebras in Program Synthesis"
collection: publications
category: manuscripts
permalink: /publication/OOPSLA25
excerpt: ''
date: 2025-10-09
venue: 'Proceedings of the ACM on Programming Languages, Volume 9, Issue OOPSLA2 (OOPSLA 2025)'
doi: 'https://doi.org/10.1145/3763176'
# slidesurl: ''
paperurl: '/files/OOPSLA25.pdf'
materialurl: 'https://github.com/StudyingFather/mole'
citation: 'Guanlin Chen<a href="#star">*</a>, Ruyi Ji<a href="#star">*</a>, <b>Shuhao Zhang</b><a href="#star">*</a>, Yingfei Xiong. Tunneling Through the Hill: Multi-Way Intersection for Version-Space Algebras in Program Synthesis. <em>Proceedings of the ACM on Programming Languages, Volume 9, Issue OOPSLA2</em>, Pages 3508-3532.'
footnote: '<em id="star">* equal contribution</em>'
---

Version space algebra (VSA) is an effective data structure for representing sets of programs and has been extensively used in program synthesis. Despite this success, a crucial shortcoming of VSA-based synthesis is its inefficiency when processing many examples. Given a set of IO examples, a typical VSA-based synthesizer runs by first constructing an individual VSA for each example and then iteratively intersecting these VSAs one by one. However, the intersection of two VSAs can be much larger than the original ones -- this effect accumulates during the iteration, making the scale of intermediate VSAs quickly explode.
In this paper, we aim to reduce the cost of intersecting VSAs in synthesis. We investigate the process of the iterative intersection and observe that, although this process may construct some huge intermediate VSAs, its final VSA is usually small in practice because only a few programs can pass all examples. Utilizing this observation, we propose the approach of multi-way intersection, which directly intersects multiple small VSAs into the final result, thus avoiding the previous bottleneck of constructing huge intermediate VSAs. Furthermore, since the previous intersection algorithm is inefficient for multiple VSAs, we design a novel algorithm to avoid most unnecessary VSA nodes. We integrated our approach into two SOTA VSA-based synthesizers: a general synthesizer based on VSA and a specialized one for the string domain, Blaze. We evaluate them over 4 different datasets, 994 synthesis tasks; the results show that our approach can significantly improve the performance of VSA-based synthesis, with up to 105 more tasks solved and a speedup of 7.36 times.
