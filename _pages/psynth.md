---
permalink: /projects/psynth/
title: "Program Synthesis via Search & Learning"
author_profile: true
---

This project aims to explore intelligent techniques to improve the traditional search-based techniques for Program Synthesis. Program Synthesis is the task of automatically finding programs from the underlying programming language that satisfy user intent expressed in some form of constraints or specifications. This project’s main objective is to develop and improve methods to synthesize programs, putting minimal human knowledge into the system. The existing methods have much scope for improvement, and we are indeed quite far from *automated programming*. This work aims to contribute in this direction.

Within the Programming Languages (PL) community, program synthesis is typically solved using *enumerative search*, finding correct programs for a given specification by naively enumerating candidates until a satisfying program is found. Various methods have been devised to do this efficiently and scalably. However, using traditional search-based techniques is often insufficient for achieving good performance in terms of computational complexity, resources, etc. The program search space for program synthesis is generally huge. Using learning-based methods (from deep learning and deep reinforcement learning), we can identify certain attributes or features from the input-output specification, which can be used to narrow down or rank different programs to choose the most suitable program. 

There are two parts of this project:

1. Implementing and improving the existing supervised deep learning-based methods for program synthesis like [DeepCoder](https://arxiv.org/abs/1611.01989), [RobustFill](https://arxiv.org/abs/1703.07469), [TF-Coder](https://arxiv.org/abs/2003.09040), etc.

2. To overcome the problems associated with the above methods (like unavailability of a large number of input-output examples, complexity of the program space, and lack of generalization to other domains), we aim to combine *search* and *learning*. Here we use priority-tree search algorithms like Monte Carlo Tree Search ([MCTS](https://en.wikipedia.org/wiki/Monte_Carlo_tree_search)), augmented using reinforcement learning methods. The searching part can efficiently cut down the program search space by pruning irrelevant regions in the space. The learning part is used to assign priority and decide which part to omit and which to explore.