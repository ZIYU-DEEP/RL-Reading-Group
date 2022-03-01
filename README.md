# RL Reading Group
⛄️ *Last updated on December, 2021.*

This is a repository for RL paper reading. It will *not* be a comprehensive list of all relevant papers. Topics are rough now; feel free to modify or increase anytime:
<!-- - *[General RL Theory](#1-rl-theory)* -->
- [Offline RL](#-offline-rl)
- [RL & Information Theory](#-rl--information-theory)
    - [Principle of Maximum Entropy](#-principle-of-maximum-entropy)
    - [Principle of Rate Reduction](#-principle-of-rate-reduction)
    - [Principle of Information Bottleneck](#-principle-of-information-bottleneck)
- [RL & Game Theory (and MARL)](#-rl--game-theory-and-marl)
- [RL & Representation Learning](#-rl--representation-learning)
- [Dueling/Preference RL](#-duelingpreference-rl-pbrl)
- [Unclassified Papers](#-unclassified-papers)
- [Miscellaneous: Blogs, People, Courses, etc.](#-miscellaneous)

Comments may be added directly below each paper, or as a separate file in the [notes](https://github.com/ZIYU-DEEP/RL-Reading-Group/tree/main/notes) folder. We can use emoji to mark certain papers if needed, like 🔘 for the discussed ones, 🔛 for papers in reading/discussion, 🔝 for important ones, 👽 for interesting ones which you plan to read shortly, 💤 for dull ones, etc.

<!-- ## 1. General RL Theory -->

## 🕹 Offline RL
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



## 🕹 RL & Information Theory
> Einstein said, “*Everything should be made as simple as possible, but no simpler.*”, or more precisely, “*It can scarcely be denied that **the supreme goal of all theory is to make the irreducible basic elements as simple and as few as possible**.*”
>
> The key characteristic of information theory is **simplicity**. Such simplicity usually endows the resulting principles with striking generality and practical effectiveness, helping us to unify diverse findings and understand fundamental mechanisms of the nature, and providing a promising direction on designing intelligent agents.

### 👾 Principle of Maximum Entropy
> This simple principle asks human to confess their ignorance.
Confronting the world of data, you could have numerous models, asnd this principle asks you to choose the *unique* model that possess the maximum entropy, i.e., you generally assume that different things are of equal probability.
> - From the designer's perspective, it asks you to choose the most diverse world model.
> - From the agent's perspective, it asks you to act the most randomly.
> - In practice, this principle can either serve as a constraint, or a direct objective to be optimized along with the original goal (e.g., maximum return).
> - Mathematically, the Principle of Maximum Entropy is usually relevant to the Exponential Family of probability distribution.

**Maximum Entropy Inverse Reinforcement Learning** [[link](https://www.aaai.org/Papers/AAAI/2008/AAAI08-227.pdf)] \
Brian D. Ziebart, Andrew Maas, J.Andrew Bagnell, Anind K. Dey\
*AAAI, 2008*

**Soft Actor-Critic: Off-Policy Maximum Entropy Deep Reinforcement Learning with a Stochastic Actor** [[link](http://proceedings.mlr.press/v80/haarnoja18b)] \
Tuomas Haarnoja, Aurick Zhou, Pieter Abbeel, Sergey Levine\
*ICML, 2018*

🔛 **Reinforcement Learning and Control as Probabilistic Inference: Tutorial and Review** [[link](https://arxiv.org/abs/1805.00909)] [[slides](https://jackhaha363.github.io/talk/control_as_inf/slides.pdf)] [[rap](https://www.youtube.com/watch?v=IAJ1LywY6Zg)] [[lecture](https://www.youtube.com/watch?v=oqvTC1rTjg8&list=PLkFD6_40KJIxJMR-j5A1mkxK26gh_qg37&index=12)] [[lecture notes](http://rail.eecs.berkeley.edu/deeprlcourse-fa18/static/slides/lec-15.pdf)] \
Sergey Levine\
*Preprint, 2018*

**Maximum Entropy-Regularized Multi-Goal Reinforcement Learning** [[link](http://proceedings.mlr.press/v97/zhao19d.html)] \
Rui Zhao, Xudong Sun, Volker Tresp\
*ICML, 2019*

**Maximum Entropy Gain Exploration for Long Horizon Multi-goal Reinforcement Learning** [[link](http://proceedings.mlr.press/v119/pitis20a.html)] \
Silviu Pitis, Harris Chan, Stephen Zhao, Bradly Stadie, Jimmy Ba\
*ICML, 2020*

**Maximum Entropy RL (Provably) Solves Some Robust RL Problems** [[link](https://arxiv.org/abs/2103.06257)] [[blog](https://bair.berkeley.edu/blog/2021/03/10/maxent-robust-rl/)] \
Benjamin Eysenbach, Sergey Levine\
*Preprint, 2021*


### 👾 Principle of Rate Reduction
> The high-level idea of this line of work is probably that: we can learn efficiently just through a latent (low-dimensional) representation of the environment. The theoretical framework can trace back to Claude Shannon's communication system and rate-distortion theory. It may also connects to the state representation learning of RL.

**World Models** [[link](https://arxiv.org/abs/1803.10122)] [[code](https://github.com/hardmaru/WorldModelsExperiments)] \
David Ha, Jürgen Schmidhuber\
*NeurIPS, 2018*

**Information-Directed Exploration for Deep Reinforcement Learning** [[link](https://openreview.net/forum?id=Byx83s09Km)] \
Nikolay Nikolov, Johannes Kirschner, Felix Berkenkamp, Andreas Krause\
*ICLR, 2019*
<!-- <br> -->

**Deciding What to Learn: A Rate-Distortion Approach** [[link](https://dilipa.github.io/papers/icml21_blasts.pdf)] \
Dilip Arumugam, Benjamin Van Roy\
*ICML, 2021*

**The Value of Information When Deciding What to Learn** [[link](https://arxiv.org/abs/2110.13973)] \
Dilip Arumugam, Benjamin Van Roy\
*NeurIPS, 2021*
<!-- <br> -->

<!-- **** [[link]()] \
\
*Preprint, 2021* -->

### 👾 Principle of Information Bottleneck
**InfoBot: Transfer and Exploration via the Information Bottleneck** [[paper](https://openreview.net/forum?id=rJg8yhAqKm)] [[code](https://github.com/maximecb/gym-minigrid)]\
Anirudh Goyal, Riashat Islam, DJ Strouse, Zafarali Ahmed, Hugo Larochelle, Matthew Botvinick, Yoshua Bengio, Sergey Levine\
*ICLR, 2019*
> The idea is simply to constrain the dependence on a certain goal, so that the agent can learn a *default behavior*.
> - This done by introducing $- \beta I(A ; G \mid S)$ or equivalently $- \beta D_{\mathrm{KL}}\left[\pi_{\theta}(A \mid S, G) \mid \pi_{0}(A \mid S)\right]$ in the reward function, that is: $$
\begin{aligned}
J(\theta) & \equiv \mathbb{E}_{\pi_{\theta}}[r]-\beta I(A ; G \mid S) \\
&=\mathbb{E}_{\pi_{\theta}}\left[r-\beta D_{\mathrm{KL}}\left[\pi_{\theta}(A \mid S, G) \mid \pi_{0}(A \mid S)\right]\right].
\end{aligned}
$$

**Generalization in Reinforcement Learning with Selective Noise Injection and Information Bottleneck** [[link](https://arxiv.org/abs/1910.12911)] [[code](https://github.com/microsoft/IBAC-SNI)] [[talk](https://www.youtube.com/watch?v=tWtM4Dq05ZA)]\
Maximilian Igl, Kamil Ciosek, Yingzhen Li, Sebastian Tschiatschek, Cheng Zhang, Sam Devlin, Katja Hofmann\
*NeurIPS, 2019*

**Learning Task-Driven Control Policies via Information Bottlenecks** [[link](https://arxiv.org/abs/2002.01428)] [[spotlight talk](https://www.youtube.com/watch?v=nzLyRHON24E)]\
Vincent Pacelli, Anirudha Majumdar\
*RSS, 2020*

🐤 **The Bottleneck Simulator: A Model-based Deep Reinforcement Learning Approach** [[journal '20](https://www.jair.org/index.php/jair/article/view/12463/26616)] [[arxiv '18](https://arxiv.org/abs/1807.04723)]
Iulian Vlad Serban, Chinnadhurai Sankar, Michael Pieper, Joelle Pineau, Yoshua Bengio\
*Journal of Artificial Intelligence Research (JAIR), 2020*

**Learning Robust Representations via Multi-View Information Bottleneck** [[link](https://openreview.net/forum?id=B1xwcyHFDr)] [[code](https://github.com/mfederici/Multi-View-Information-Bottleneck)] [[talk](https://iclr.cc/virtual_2020/poster_B1xwcyHFDr.html)]\
Marco Federici, Anjan Dutta, Patrick Forré, Nate Kushman, Zeynep Akata\
*ICLR, 2020*

**DRIBO: Robust Deep Reinforcement Learning via Multi-View Information Bottleneck** [[paper](https://openreview.net/forum?id=Py8WbvKH_wv)] [[code](https://github.com/JmfanBU/DRIBO)]\
Jiameng Fan, Wenchao Li\
*Rejected by ICLR, 2022*

**Learning Representations in Reinforcement Learning: an Information Bottleneck Approach** [[link](https://openreview.net/forum?id=Syl-xpNtwS)] [[code](https://github.com/AnonymousSubmittedCode/SVIB)]\
Yingjun Pei, Xinwen Hou\
*Rejected by ICLR, 2020*

**Dynamics Generalization via Information Bottleneck in Deep Reinforcement Learning** [[link](https://arxiv.org/abs/2008.00614)]\
Xingyu Lu, Kimin Lee, Pieter Abbeel, Stas Tiomkin\
*ArXiv, 2020*

**Dynamic Bottleneck for Robust Self-Supervised Exploration** [[paper](https://openreview.net/forum?id=-t6TeG3A6Do)] [[code](https://github.com/Baichenjia/DB)]\
Chenjia Bai, Lingxiao Wang, Lei Han, Animesh Garg, Jianye HAO, Peng Liu, Zhaoran Wang\
*NeurIPS, 2021*
> - The high-level idea is to first generate a dynamics-relevant representation $Z_{t}$, then impose a bottleneck on dynamics, in order to through away the dynamics-irrelevant information.
> - That is, $\min I([S_t, A_t]; Z_t)$, and $\max I(Z_t; S_{t+1})$.





### 👾 Others
**EMI: Exploration with Mutual Information** [[link](https://arxiv.org/abs/1810.01176)] \
Hyoungseok Kim, Jaekyeom Kim, Yeonwoo Jeong, Sergey Levine, Hyun Oh Song\
*ICML, 2019*

**Reinforcement Learning, Bit by Bit**\
Xiuyuan Lu, Benjamin Van Roy, Vikranth Dwaracherla, Morteza Ibrahimi, Ian Osband, Zheng Wen\
*ArXiv, 2022*\
[[paper](https://arxiv.org/abs/2103.04047)]
> - The high level idea comes from Posterior Sampling, that we sample the environment from a maintained posterior at the beginning of each episode, and then take the action which minimizing the information ratio.
> - The information ratio is defined by: $$\Gamma_{\tau, t}=\frac{\mathbb{E}\left[V_{*}\left(H_{t}\right)-Q_{*}\left(H_{t}, A_{t}\right)\right]^{2}}{\left(\mathbb{I}\left(\chi ; \mathcal{E} \mid P_{t}\right)-\mathbb{I}\left(\chi ; \mathcal{E} \mid P_{t+\tau}\right)\right) / \tau}.$$
> - This can be view as a very classical exploration-exploitation tradeoff. The numerator represents the immediate shortfall, while the nominator represents the information gain about the environment.
> - :baby_chick:: A potential improvement might be incorporating information bottleneck in the denominator part. That is, we may not need to learn that much from the environment: we only want learn those to be relevant to our objective, and discard those irrelevant.

## 🕹 RL & Game Theory (and MARL)
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


## 🕹 RL & Representation Learning
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

## 🕹 Dueling/Preference RL (PbRL)
> Generally, this line of work considers RL problems without explicitly defined reward for each `(state, action)` paper. In the standard setting, the agent will play a duel (i.e, two trajectories) during each episode, and will receive only a **preference feedback** (e.g., 0/1) for the two **trajectories** at the end. This setting is more general and eschews some of the issues in traditional reward learning or inverse RL literature. The techniques developed can be applied to various domains, like multi-objective trade-offs (e.g., the NIPS '17 one below.)

**Deep Reinforcement Learning from Human Preferences** [[link](https://arxiv.org/pdf/1706.03741.pdf)] \
Paul Christiano, Jan Leike, Tom B. Brown, Miljan Martic, Shane Legg, Dario Amodei\
*NIPS, 2017*

**A Generalized Algorithm for Multi-Objective Reinforcement Learning and Policy Adaptation** [[link](https://arxiv.org/abs/1908.08342)] [[code](https://github.com/RunzheYang/MORL)] \
Runzhe Yang, Xingyuan Sun, Karthik Narasimhan\
*NIPS, 2019*
> - This paper is on **multi-objective reinforcement learning (MORL)** with **linear preferences**, with the goal of enabling **few-shot adaptation** to new tasks.
> - A slightly similar work on MOBO in the same venue: [Multi-objective Bayesian Optimization with Preferences over Objectives](https://proceedings.neurips.cc/paper/2019/file/a7b7e4b27722574c611fe91476a50238-Paper.pdf).

👽 **Dueling Posterior Sampling for Preference-based Reinforcement Learning** [[link](http://proceedings.mlr.press/v124/novoseller20a/novoseller20a.pdf)] [[code](https://github.com/ernovoseller/DuelingPosteriorSampling)] \
Ellen R. Novoseller, Yibing Wei, Yanan Sui, Yisong Yue, Joel W. Burdick\
*UAI, 2020*
> Information ratio is used in the proof as well.

**Preference-based Reinforcement Learning with Finite-Time Guarantees** [[link](https://arxiv.org/abs/2006.08910)] \
Yichong Xu, Ruosong Wang, Lin F. Yang, Aarti Singh, Artur Dubrawski\
*NeurIPS (spotlight), 2020*

👽 **Dueling RL: Reinforcement Learning with Trajectory Preferences** [[link](https://arxiv.org/pdf/2111.04850.pdf)] \
Aldo Pacchiano, Aadirupa Saha, and Jonathan Lee\
*Preprint, 2021*
> One interesting future direction raised in this paper is the preference over a *set*. It is more general than duel, since the agent can play a set of trajectories instead of just two. The non-transitive preference (e.g., [a dice case](https://www.wikiwand.com/en/Intransitive_dice)) may be relevant here.

**On the Theory of Reinforcement Learning with Once-per-Episode Feedback** [[link](https://arxiv.org/abs/2105.14363)] \
Niladri S. Chatterji, Aldo Pacchiano, Peter L. Bartlett, Michael I. Jordan\
*Preprint, 2021*




## 🕹 Unclassified Papers
🔛 **Machine Theory of Mind** [[link](https://arxiv.org/abs/1802.07740)] \
Neil C. Rabinowitz, Frank Perbet, H. Francis Song, Chiyuan Zhang, S.M. Ali Eslami, Matthew Botvinick\
*ICML, 2018*
<br>

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


**Learning the Arrow of Time for Problems in Reinforcement Learning** [[link](https://openreview.net/forum?id=rylJkpEtwS)] [[talk](https://iclr.cc/virtual_2020/poster_rylJkpEtwS.html)] \
Nasim Rahaman, Steffen Wolf, Anirudh Goyal, Roman Remme, Yoshua Bengio\
*ICLR, 2021*
> The notion of the arrow of time looks to be captivating, which is a function *tends* to increase as the MDP steps forward, just like the entropy increase principle. The agent will be rewarded for trajectories which decrease such an arrow, i.e., push the orderless to the ordered, like Sisyphus.









## 🕹 Miscellaneous
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









<!-- **** [[link]()] \
\
*Preprint, 2021*
<br> -->
