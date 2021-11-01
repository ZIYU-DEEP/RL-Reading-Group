# RL Reading Group
*Last updated on November, 2021.*

This is a repository for RL paper reading. It will *not* be a comprehensive list of all relevant papers. Topics are rough now; feel free to modify or increase anytime:
<!-- - *[General RL Theory](#1-rl-theory)* -->
- [Offline RL](#1-offline-rl)
- [RL & Game Theory (and MARL)](#2-rl--game-theory-and-marl)
- [RL & Information Theory](#3-rl--information-theory)
- [RL & Representation Learning](#4-rl--representation-learning)
- [Miscellaneous: Blogs, People, Courses, etc.](#5-miscellaneous)

Comments may be added directly below each paper, or as a separate file in the [notes](https://github.com/ZIYU-DEEP/RL-Reading-Group/tree/main/notes) folder. We can use emoji to mark certain papers if needed, like 🔘 for the discussed ones, 🔛 for papers in reading/discussion, 🔝 for important ones, 👽 for interesting ones which you plan to read shortly, 💤 for dull ones, etc.

<!-- ## 1. General RL Theory -->

## 1. Offline RL
**[Awesome Offline RL](https://github.com/hanjuku-kaso/awesome-offline-rl)**\
Haruka Kiyohara, Yuta Saito, Guoyu Yang
<!-- <br> -->

**Offline Reinforcement Learning: Tutorial, Review, and Perspectives on Open Problems** [[link](https://arxiv.org/abs/2005.01643)] [[tutorial](https://sites.google.com/view/offlinerltutorial-neurips2020/home)] [[video](https://slideslive.com/38935785)] \
Sergey Levine, Aviral Kumar, George Tucker, Justin Fu\
*Preprint, 2020*
<!-- <br> -->

👽 **MOPO: Model-based Offline Policy Optimization** [[link](https://arxiv.org/abs/2005.13239)] [[code](https://github.com/tianheyu927/mopo)] \
Tianhe Yu, Garrett Thomas, Lantao Yu, Stefano Ermon, James Zou, Sergey Levine, Chelsea Finn, Tengyu Ma\
*NeurIPS, 2020*
<!-- <br> -->

**Bellman-Consistent Pessimism for Offline Reinforcement Learning** [[link](https://arxiv.org/abs/2106.06926)] \
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

## 2. RL & Game Theory (and MARL)
> Roughly speaking, major works consider to understand your opponents/collaborators, by explicitly estimating other agents' behaviors, or promoting communication (information sharing) between agents. However, there are also papers claiming that learning in a single-agent way may already be sufficient for you to exceed in the multi-agent environment.

👽 **An Overview of Multi-Agent Reinforcement Learning from Game Theoretical Perspective** [[link](https://arxiv.org/abs/2011.00583)] \
Yaodong Yang, Jun Wang\
*Preprint, 2021*

**Multi‑agent Deep Reinforcement Learning: a Survey** [[link](https://link.springer.com/content/pdf/10.1007/s10462-021-09996-w.pdf)] \
Sven Gronauer, Klaus Diepold\
*Artificial Intelligence Review, 2021*

**Value-Decomposition Networks For Cooperative Multi-Agent Learning** [[link](https://arxiv.org/abs/1706.05296)] \
Peter Sunehag, Guy Lever, Audrunas Gruslys, Wojciech Marian Czarnecki, Vinicius Zambaldi, Max Jaderberg, Marc Lanctot, Nicolas Sonnerat, Joel Z. Leibo, Karl Tuyls, Thore Graepel\
*AAMAS, 2017*

👽 **A Game Theoretic Framework for Model Based Reinforcement Learning** [[link](https://arxiv.org/abs/2004.07804)] \
Aravind Rajeswaran, Igor Mordatch, Vikash Kumar\
*ICML, 2020*

**Cooperative Exploration for Multi-Agent Deep Reinforcement Learning** [[link](https://arxiv.org/abs/2107.11444)] [[website](https://ioujenliu.github.io/CMAE/)] [[video](https://youtu.be/rQZHawgqgsk)] \
Iou-Jen Liu, Unnat Jain, Raymond A. Yeh, Alexander G. Schwing\
*ICML, 2021*

👽 **IPPO: Is Independent Learning All You Need in the StarCraft Multi-Agent Challenge?** [[link](https://arxiv.org/abs/2011.09533)] \
Christian Schroeder de Witt, Tarun Gupta, Denys Makoviichuk, Viktor Makoviychuk, Philip H.S. Torr, Mingfei Sun, Shimon Whiteson\
*Preprint, 2020*
> Do we really need to model others' behavior? Unlike popular cooperative MARL papers which usually involves a *centralized* value function, IPPO lets each agent just estimate its own *local* value function, which achieves compatible results with SOTA models.
>
> I feel this aligns with the very beginning idea of Adam Smith on the [invisible hand](https://www.wikiwand.com/en/Invisible_hand), i.e., better social welfare stems from individual just acting in *their own self-interests*. Plus, a centralized value function may not be a good idea, as individual utility function can hardly be added up in complex environment. It might be interesting to examine the problem from an economics perspective, e.g., if there exists [market failure](https://www.wikiwand.com/en/Market_failure) phenomena in the independent learning, and how we may incorporate certain regularizations to improve market (learning) efficiency.

**MAPPO: The Surprising Effectiveness of PPO in Cooperative, Multi-Agent Games** [[link](https://arxiv.org/abs/2103.01955)] [[blog](https://bair.berkeley.edu/blog/2021/07/14/mappo/)] [[code](https://github.com/marlbenchmark/on-policy)] \
Chao Yu, Akash Velu, Eugene Vinitsky, Yu Wang, Alexandre Bayen, Yi Wu\
*Preprint, 2021*
> This paper is like a follow-up work on IPPO. The critic part of MAPPO uses the (agent-specific) *global state* as the input, unlike the observations used in IPPO.
>
> Several algorithmic tricks are discussed in this paper, like value normalization, action masking, etc.

<!-- **** [[link]()] \
\
*Preprint, 2021* -->


## 3. RL & Information Theory
> The high-level idea of this line of work is probably that: we can learn efficiently just through a latent (low-dimensional) representation of the environment. The theoretical framework can trace back to Claude Shannon's communication system and rate-distortion theory. It may also connects to the state representation learning of RL.

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
*Preprint, 2021* -->


## 4. RL & Representation Learning
**Provably Efficient RL with Rich Observations via Latent State Decoding** [[link](https://arxiv.org/abs/1901.09018)] \
Simon S. Du, Akshay Krishnamurthy, Nan Jiang, Alekh Agarwal, Miroslav Dudík, John Langford\
*ICML, 2019*

**Is a Good Representation Sufficient for Sample Efficient Reinforcement Learning?** [[link](https://arxiv.org/abs/1910.03016)] \
Simon S. Du, Sham M. Kakade, Ruosong Wang, Lin F. Yang\
*ICLR, 2020*

**Dream to Control: Learning Behaviors by Latent Imagination** [[link](https://openreview.net/forum?id=S1lOTC4tDS)] [[blog](https://ai.googleblog.com/2020/03/introducing-dreamer-scalable.html)] [[website](https://danijar.com/project/dreamer/)] [[video](https://youtu.be/BDxRNnhPTlU)] \
Danijar Hafner, Timothy Lillicrap, Jimmy Ba, Mohammad Norouzi\
*ICLR (spotlight), 2020*

**Decoupling Representation Learning from Reinforcement Learning** [[link](http://proceedings.mlr.press/v139/stooke21a.html)] \
Adam Stooke, Kimin Lee, Pieter Abbeel, Michael Laskin \
*ICML, 2021*

**Learning Invariant Representations for Reinforcement Learning without Reconstruction** [[link](https://arxiv.org/abs/2006.10742)] \
Amy Zhang, Rowan McAllister, Roberto Calandra, Yarin Gal, Sergey Levine\
*ICLR (oral), 2021*

**Representation Learning for Online and Offline RL in Low-rank MDPs** [[link](https://arxiv.org/abs/2110.04652)] \
Masatoshi Uehara, Xuezhou Zhang, Wen Sun\
*Preprint, 2021*


<!-- **** [[link]()] \
\
*Preprint, 2021* -->







## 5. Miscellaneous
### Courses
- [CMPUT 653 Theoretical Foundations of Reinforcement Learning](https://rltheory.github.io/) by [Csaba Szepesvári](https://sites.ualberta.ca/~szepesva/) at the University of Alberta.
- [CS 598 Statistical Reinforcement Learning](https://nanjiang.cs.illinois.edu/cs598/) by [Nan Jiang](https://nanjiang.cs.illinois.edu/) at UIUC.
- [CS 6789: Foundations of Reinforcement Learning](https://wensun.github.io/CS6789_fall_2021.html) by [Wen Sun](https://wensun.github.io/) at Cornell University and [Sham Kakade](https://homes.cs.washington.edu/~sham/) at University of Washington, with a book named [Reinforcement Learning: Theory and Algorithms](https://rltheorybook.github.io/).
### Seminars and Workshops
- [RL Theory Seminars](https://sites.google.com/view/rltheoryseminars/home), and its [YouTube page](https://www.youtube.com/c/RLtheory).
- [Statistical Foundations of Reinforcement Learning](https://rltheorybook.github.io/colt21tutorial) at COLT 2021.
- [Offline Reinforcement Learning Tutorial](https://sites.google.com/view/offlinerltutorial-neurips2020/home) at NeurIPS 2020.
- [Offline Reinforcement Learning Workshop](https://offline-rl-neurips.github.io/papers.html) at NeurIPS 2020, with a bunch of videos on workshop papers.
- [Smooth Games Optimization and ML Workshop](https://sgo-workshop.github.io/) at NeurIPS 2019.
- OpenAI's [Key Papers in Deep RL](https://spinningup.openai.com/en/latest/spinningup/keypapers.html) and a [summary](https://github.com/RPC2/DRL_paper_summary), 2018.

### Unclassified Papers
**OptNet: Differentiable Optimization as a Layer in Neural Networks** [[link](http://proceedings.mlr.press/v70/amos17a/amos17a.pdf)] \
Brandon Amos, J. Zico Kolter\
*ICML, 2017*

**Provably Efficient Exploration for RL with Unsupervised Learning** [[link](https://arxiv.org/abs/2003.06898)] [[slides](https://drive.google.com/file/d/1lVLTongo_cK9qfsWwb63lIn06SrYiOY8/view)] [[talk](https://youtu.be/kaQSX7oSyWg)] \
Fei Feng, Ruosong Wang, Wotao Yin, Simon S. Du, Lin F. Yang\
*NeurIPS, 2020*


**A Unified Switching System Perspective and O.D.E. Analysis of Q-Learning Algorithms** [[link](https://arxiv.org/abs/1912.02270)] [[slides](https://arxiv.org/abs/1912.02270)] [[talk](https://youtu.be/3DLndSERBh8)] \
Donghwan Lee, Niao He\
*NeurIPS, 2020*

👽 **Making Sense of Reinforcement Learning and Probabilistic Inference** [[link](https://openreview.net/forum?id=S1xitgHtvS)] \
Brendan O'Donoghue, Ian Osband, Catalin Ionescu\
*ICLR, 2020*
> This paper generalizes the *RL optimization problem* to be a *Bayesian inference problem*, and proposes a coherent framework to minimize Bayes regret. This approach better integrates the exploration concerns in RL which is often ignored in traditional works.
>
> This paper also connects to Surgey Levine's well cited survey: [Reinforcement Learning and Control as Probabilistic Inference: Tutorial and Review](https://arxiv.org/abs/1805.00909), while this one further emphasizes the role of epistemic uncertainty in policy design.

**Reinforcement Learning and Control as Probabilistic Inference: Tutorial and Review** [[link](https://arxiv.org/abs/1805.00909)] [[slides](https://jackhaha363.github.io/talk/control_as_inf/slides.pdf)] [[rap](https://www.youtube.com/watch?v=IAJ1LywY6Zg)] \
Sergey Levine\
*Preprint, 2021*

**Hypermodels for Exploration** [[link](https://openreview.net/forum?id=ryx6WgStPB)] \
Vikranth Dwaracherla, Xiuyuan Lu, Morteza Ibrahimi, Ian Osband, Zheng Wen, Benjamin Van Roy\
*ICLR, 2020*
> The idea stems from Thompson Sampling. Simply put, Ensemble DQN is hard to train due to its high parameter complexity; this paper proposes to just maintain a hyper network, which generates the corresponding parameters for the Ensemble DQN while encoding the same information.

**Learning to Plan in High Dimensions via Neural Exploration-Exploitation Trees** [[link](https://arxiv.org/abs/1903.00070)] [[talk](https://papertalk.org/papertalks/3941)] \
Binghong Chen, Bo Dai, Qinjie Lin, Guo Ye, Han Liu, Le Song\
*ICLR (spotlight), 2020*
> This may potentially be relevant to the UFODT paper, as well as the NeurIPS 2021 paper: [The Value of Information When Deciding What to Learn](https://arxiv.org/abs/2110.13973).

**Lottery Tickets in RL and NLP** [[link](https://openreview.net/forum?id=S1xnXRVFwH)] \
Haonan Yu, Sergey Edunov, Yuandong Tian, Ari S. Morcos\
*ICLR, 2020*
<br>

**Learning the Arrow of Time for Problems in Reinforcement Learning** [[link](https://openreview.net/forum?id=rylJkpEtwS)] [[talk](https://iclr.cc/virtual_2020/poster_rylJkpEtwS.html)] \
Nasim Rahaman, Steffen Wolf, Anirudh Goyal, Roman Remme, Yoshua Bengio\
*ICLR, 2021*
> The notion of the arrow of time looks to be captivating, which is a function *tends* to increase as the MDP steps forward, just like the entropy increase principle. The agent will be rewarded for trajectories which decrease such an arrow, i.e., push the orderless to the ordered, like Sisyphus.









<!-- **** [[link]()] \
\
*Preprint, 2021*
<br> -->
