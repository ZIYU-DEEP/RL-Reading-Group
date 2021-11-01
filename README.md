# RL Reading Group
A repository for RL paper reading. This will not be a comprehensive list of all relevant papers. Topics are rough now and feel free to modify or increase anytime:
<!-- - *[General RL Theory](#1-rl-theory)* -->
- *[Offline RL](#1-offline-rl)*
- *[RL & Information Theory](#2-rl--information-theory)*
- *[RL & Game Theory](#3-rl--game-theory)*
- *[Miscellaneous: Blogs, People, Courses, etc.](#4-miscellaneous)*

Comments/notes may be added directly below each paper, or as a separate file in the [notes]() folder. We can use emoji to mark certain papers if needed, like using 🔘 for the read and discussed ones, 🔛 for papers in reading/discussion, 🔝 for important ones, 💤 for dull ones, 👽 for interesting ones which you plan to read later, etc.

<!-- ## 1. General RL Theory -->

## 1. Offline RL
**[Awesome Offline RL Collection](https://github.com/hanjuku-kaso/awesome-offline-rl)**\
Haruka Kiyohara, Yuta Saito, Guoyu Yang
<!-- <br> -->

**Offline Reinforcement Learning: Tutorial, Review, and Perspectives on Open Problems** [[link](https://arxiv.org/abs/2005.01643)] [[tutorial](https://sites.google.com/view/offlinerltutorial-neurips2020/home)] [[video](https://slideslive.com/38935785)] \
Sergey Levine, Aviral Kumar, George Tucker, Justin Fu\
*Preprint, 2020*
<!-- <br> -->

👽**MOPO: Model-based Offline Policy Optimization** [[link](https://arxiv.org/abs/2005.13239)] [[code](https://github.com/tianheyu927/mopo)] \
Tianhe Yu, Garrett Thomas, Lantao Yu, Stefano Ermon, James Zou, Sergey Levine, Chelsea Finn, Tengyu Ma\
*NeurIPS, 2020*
<!-- <br> -->

**Bellman-consistent Pessimism for Offline Reinforcement Learning** [[link](https://arxiv.org/abs/2106.06926)] \
Tengyang Xie, Ching-An Cheng, Nan Jiang, Paul Mineiro, Alekh Agarwal\
*NeurIPS (oral), 2021*
<!-- <br> -->

**Bridging Offline Reinforcement Learning and Imitation Learning: A Tale of Pessimism** [[link](https://arxiv.org/abs/2103.12021)] [[slides](https://drive.google.com/file/d/1cA7AJX19BjNcq6xLjfHWGJnggdVWnbUJ/view?usp=sharing)] [[talk](https://youtu.be/oK0iPImC6KI)] \
Paria Rashidinejad, Banghua Zhu, Cong Ma, Jiantao Jiao, Stuart Russell\
*NeurIPS, 2021*
<!-- <br> -->

**Is Pessimism Provably Efficient for Offline RL?** [[link](https://arxiv.org/abs/2012.15085)] [[slides](https://icml.cc/media/icml-2021/Slides/10409.pdf)]\
Ying Jin, Zhuoran Yang, Zhaoran Wang\
*ICML, 2021*
<!-- <br> -->

**Towards Hyperparameter-free Policy Selection for Offline Reinforcement Learning** [[link](https://arxiv.org/pdf/2110.14000.pdf)] [[code]()] \
Siyuan Zhang, Nan Jiang\
*NeurIPS, 2021*
<!-- <br> -->


<!-- **Offline Reinforcement Learning with Implicit Q-Learning** [[abs](https://arxiv.org/abs/2110.06169)] [[code](https://github.com/ikostrikov/implicit_q_learning)]\
Ilya Kostrikov, Ashvin Nair, Sergey Levine\
*Preprint, 2021*
<br> -->


## 2. RL & Information Theory
> The high-level idea of this line of work is probably that: we can learn efficiently just through a latent (low-dimensional) representation of the environment. The theoretical framework can trace back to Claude Shannon's communication system and rate-distortion theory. This may also connects to the state representation learning of RL.

**World Models** [[link](https://arxiv.org/abs/1803.10122)] [[code](https://github.com/hardmaru/WorldModelsExperiments)] \
David Ha, Jürgen Schmidhuber\
*NeurIPS, 2018*
<!-- <br> -->

**Information-Directed Exploration for Deep Reinforcement Learning** [[link](https://openreview.net/forum?id=Byx83s09Km)] \
Nikolay Nikolov, Johannes Kirschner, Felix Berkenkamp, Andreas Krause\
*ICLR, 2019*
<!-- <br> -->

**Deciding What to Learn: A Rate-Distortion Approach** [[link](https://dilipa.github.io/papers/icml21_blasts.pdf)] \
Dilip Arumugam, Benjamin Van Roy\
*ICML, 2021*
<!-- <br> -->

<!-- **** [[link]()] \
\
*Preprint, 2021*
<br> -->




## 3. RL & Game Theory
👽**An Overview of Multi-Agent Reinforcement Learning from Game Theoretical Perspective** [[link](https://arxiv.org/abs/2011.00583)] \
Yaodong Yang, Jun Wang\
*Preprint, 2021*
<!-- <br> -->

👽**A Game Theoretic Framework for Model Based Reinforcement Learning** [[link](https://arxiv.org/abs/2004.07804)] \
Aravind Rajeswaran, Igor Mordatch, Vikash Kumar\
*ICML, 2020*
<!-- <br> -->

<!-- **** [[link]()] \
\
*Preprint, 2021*
<br> -->


## 4. Miscellaneous
### Courses
- **[CMPUT 653 Theoretical Foundations of Reinforcement Learning](https://rltheory.github.io/)** by [Csaba Szepesvári](https://sites.ualberta.ca/~szepesva/) at the University of Alberta.
- **[CS 598 Statistical Reinforcement Learning](https://nanjiang.cs.illinois.edu/cs598/)** by [Nan Jiang](https://nanjiang.cs.illinois.edu/) at UIUC.
- **[CS 6789: Foundations of Reinforcement Learning](https://wensun.github.io/CS6789_fall_2021.html)** by Wen Sun at Cornell University and Sham Kakade at University of Washington, with a book named [Reinforcement Learning: Theory and Algorithms](https://rltheorybook.github.io/).
### Seminars and Workshops
- **[RL Theory Seminars](https://sites.google.com/view/rltheoryseminars/home)**, and its [YouTube page](https://www.youtube.com/c/RLtheory).
- **[Offline Reinforcement Learning Tutorial](https://sites.google.com/view/offlinerltutorial-neurips2020/home)** at NeurIPS 2020.
- **[Offline Reinforcement Learning Workshop](https://offline-rl-neurips.github.io/papers.html)** at NeurIPS 2020, with a bunch of videos on workshop papers.
- **[Smooth Games Optimization and ML Workshop](https://sgo-workshop.github.io/)** at NeurIPS 2019.

### Unclassified Papers
**Provably Efficient Exploration for RL with Unsupervised Learning** [[link](https://arxiv.org/abs/2003.06898)] [[slides](https://drive.google.com/file/d/1lVLTongo_cK9qfsWwb63lIn06SrYiOY8/view)] [[talk](https://youtu.be/kaQSX7oSyWg)] \
Fei Feng, Ruosong Wang, Wotao Yin, Simon S. Du, Lin F. Yang\
*NeurIPS, 2020*


**A Unified Switching System Perspective and O.D.E. Analysis of Q-Learning Algorithms** [[link](https://arxiv.org/abs/1912.02270)] [[slides](https://arxiv.org/abs/1912.02270)] [[talk](https://youtu.be/3DLndSERBh8)] \
Donghwan Lee, Niao He\
*NeurIPS, 2020*


**Decoupling Representation Learning from Reinforcement Learning** [[link](http://proceedings.mlr.press/v139/stooke21a.html)] \
Adam Stooke, Kimin Lee, Pieter Abbeel, Michael Laskin \
*ICML, 2021*
<!-- <br> -->






<!-- **** [[link]()] \
\
*Preprint, 2021*
<br> -->
