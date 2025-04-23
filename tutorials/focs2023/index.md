# [🦊 FOCS 2023](https://focs.computer.org/2023/) Workshop: Algorithmic Aspects of High-Dimensional Probabilistic Models
## Organized by Arnab Bhattacharyya (National University of Singapore) and Clément Canonne (University of Sydney)

⏰ _Dates:_ Nov 6–7, 2023

High-dimensional probability distributions are currently omnipresent as models for complex data. Probabilistic models are used in an amazingly diverse array of data analysis tasks, from understanding sociological behavior to enabling visual object recognition, speech perception, and natural language comprehension. High-dimensional probabilistic models take various forms: classically-studied models such as multivariate Gaussians and Erdős-Rényi graphs, models with roots in statistical physics such as stochastic block models and Ising models, probabilistic graphical models such as Bayesian networks and Markov random fields, as well as the class of implicit generative models, such as generative adversarial networks and large language models, that have taken the world by storm recently. 

The goal of the proposed workshop is to highlight current trends in research on __algorithmic aspects of high-dimensional probabilistic models__. Specifically, we will focus on recent works that identify __new directions for the TCS community__, so as to encourage newcomers to delve into the important problems in the area. The workshop is particularly timely, as it is increasingly in vogue to be presented with generative models that sample from a distribution _D_, with the goal being to efficiently learn information about _D_. What are rigorous guarantees that can be made when _D_ is high-dimensional and  "complex"? Better understanding of the computational aspects of such questions can  be potentially impactful for a number of areas, e.g., security, machine learning, probabilistic programming, etc.

__Program__: All talks will take place in room __Sequoia D, 9—10:15am.__

The program will feature talks on recent and exciting results in this area, and will gather open problems in the topic from and for the participants: 

* November 6 (Day 1)
  * 9:00-9:35: [Inbal Livni Navon](http://inballn.su.domains/) (Stanford University)
    <details>

    <summary>"Indistinguishable Generative Models of Huge Objects"</summary>
    
    __Abstract:__
    In this talk I am going to discuss generative models of huge objects, from the perspective of a recent notion called outcome indistinguishability. In generative models, the goal is to generate a distribution that is similar to a specific input object (or distribution). When the input object is huge and complex and cannot be read entirely, how do we find a generative model for our object? How do we define similarity between our model and the object? In our work, we answer both questions using outcome indistinguishability. In the talk, I am going to explain what outcome indistinguishability is, and how it is helpful in our setting of learning generative models.     
    </details>

  * 9:40-10:15: [Yury Polyanskiy](https://people.lids.mit.edu/yp/homepage/) (MIT)    
    <details>
    <summary>"Likelihood-free hypothesis testing"</summary>
    
    __Abstract:__
    Modern theoretical models in particle physics, climate modeling etc often provide predictions in the form of extremely complex simulators. Thus, in order to empirically validate such theories a statistician needs to compare an experimental sample against several simulated ones, corresponding to different choices of phenomenological parameters of the theory. This area of work, known under the names of likelihood-free inference (LFI) or simulation-based inference, can be seen as extension of classical two-sample testing to more than two samples. In this talk we will present minimax sample complexities and discover the existence of a tradeoff between the sizes of experimental sample and the simulated ones, in particular showing the possibility of testing hypotheses without estimating densities. As a by-product of this tradeoff we discover (a) a universal relation between the sample complexities of goodness-of-fit (identity) testing and density estimation; (b) new methods for optimal two-sample and indentity testing based on classification accuracy.

    Joint work with Patrik Gerber (MIT) and Yanjun Han (Courant).    
    </details>
* November 7 (Day 2)
  * 9:00-9:35: [Arnab Bhattacharyya](https://www.comp.nus.edu.sg/~arnab/) (NUS)
    <details>

    <summary>"TV Distance Estimation is as easy as Probabilistic Inference"</summary>
    
    __Abstract:__
    We discuss the algorithmic problem of computing the total variation (TV) distance between two high-dimensional probability distributions.   Two highlights are:
    1. The problem of exactly computing the TV distance between two product distributions is #P-complete. This is in stark contrast with other distance measures such as KL, Chi-square, and Hellinger which tensorize over the marginals leading to efficient algorithms.
    2.  We show a novel connection between TV distance estimation and probabilistic inference. In particular, we present an efficient, structure-preserving reduction from relative approximation of TV distance to probabilistic inference over directed graphical models. This reduction leads to a fully polynomial randomized approximation scheme (FPRAS) for estimating TV distances between distributions that are defined by Bayes nets of bounded treewidth. Our approach employs a new notion of partial couplings of high-dimensional distributions, which might be of independent interest.
       
    Joint work with Sutanu Gayen (IIT Kanpur), Kuldeep Meel (Toronto & NUS), Dimitrios Myrisiotis (NUS), A. Pavan (Iowa State), and N.V. Vinodchandran (U. Nebraska Lincoln).
    </details>
  * 9:40-10:15: [Guy Van den Broeck](https://web.cs.ucla.edu/~guyvdb/) (UCLA)
    <details>

    <summary>"Tractable Probabilistic Circuits"</summary>
    
    __Abstract:__
    Probabilistic circuits represent joint distributions as computation graphs, akin to neural networks. They move beyond other deep generative models and probabilistic graphical models by guaranteeing tractable probabilistic inference for certain classes of queries: marginal probabilities, entropies, expectations, causal effects, etc. Probabilistic circuit models are now also effectively learned from data at scale, and achieve state-of-the-art results in constrained sampling from both language models and natural image distributions. This talk will overview recent developments in efficient probabilistic inference, as well as connections to the theory of probability generating polynomials.
    
    __Bio:__
    Guy Van den Broeck is an Associate Professor and Samueli Fellow at UCLA, in the Computer Science Department, where he directs the StarAI lab. His research interests are in Machine Learning, Knowledge Representation and Reasoning, and Artificial Intelligence in general. His papers have been recognized with awards from key conferences such as AAAI, UAI, KR, and OOPSLA. Guy is the recipient of an NSF CAREER award, a Sloan Fellowship, and the IJCAI-19 Computers and Thought Award.
    </details>

__Call for Open Problems:__ To suggest an open problem, please [fill this Google form](https://docs.google.com/forms/d/e/1FAIpQLSf_0me17ooezTjiVWVRgkcdJ2pAmCNxxRzZ_9WdAVJ7ojGGCg/viewform) 📋

__Dinner__: to gauge interest in a dinner 🍲 on November 6 (first day) for the workshop participants, please [fill this other Google form](https://docs.google.com/forms/d/e/1FAIpQLSdHfFUMnsq-hoFZ3HwwqfAuU2AYgDwkzMgSdZvQ9L-Z5wD0bQ/viewform) 📋
