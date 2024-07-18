---
title: Quality Diversity
author: Dennis G. Wilson
date: '2024-07-17'
tags:
  - EC
  - AI
  - algorithms
  - newsletter
---

# The Evolution of Quality Diversity in AI

This week marks the annual [Genetic and Evolutionary Computation Conference (GECCO)](https://gecco-2024.sigevo.org/), the premiere gathering in evolutionary computation (EC).
While this field has been around for decades, it may be less familiar to readers than other parts of AI like deep learning and neural networks.
EC uses biological evolution as a source of inspiration for the design of optimization algorithms; as Professor A. E. Eiben says, "given the fact that evolution can produce intelligence, it is plausible that artificial evolution can produce artificial intelligence."
EC has had high adoption in industrial settings, where it is easy to set problems up for optimization in these gradient-free methods.
And, despite its age, the field is still very much advancing and proposing new ideas.
So to celebrate this oft overlooked but fascinating branch of artificial intelligence, I want to dive into one of the more recent developments: [**Quality Diversity**](https://quality-diversity.github.io/) (QD).
This concept has the potential to change how we think about optimization problems, moving beyond finding a best solution to, instead, uncovering a collection of high-quality, diverse solutions.

The idea of optimizing towards multiple solutions is not a new one.
Multi-objective optimization (MOO) algorithms find solutions which are good, maybe even optimal, in one objective while still being good in another objective.
Many real-world problems are multi-objective; for example, think about building a bridge.
You want to reduce costs and building time, but you also want to maximize structural integrity and minimize damage to the surrounding area.
There isn't one good solution - all solutions present a trade-off between these different objectives.
Some solutions, though, will be better than many other solutions over all objectives, and algorithms search for that set of solutions.
Population-based approaches like EC are a natural fit for multi-objective optimization because they operate on multiple solutions at once.

EC has been used for multi-objective applications in chemical engineering, electric grids, and many design processes like engines, ships, and antennae.
The principles of MOO even extend into the realm of deep learning and generative AI.
In these fields, the balance between different performance metrics, such as accuracy, computational efficiency, and robustness, is crucial.
MOO techniques can help navigate these trade-offs, leading to more effective and versatile models.

## From Objectives to Diversity

Most optimization tries to reach a single, optimal solution.
Multi-objective optimization focuses on obtaining multiple solutions for a set of predefined objectives.
Quality Diversity (QD) shifts the focus towards generating a diverse set of high-quality solutions.
One of the first methods behind QD was Novelty Search, which optimizes not towards any objective but rather towards the exploration of novel behaviors.
This approach can lead to unexpected and innovative outcomes, as it encourages exploration of the solution space without being constrained by predefined goals.
By prioritizing novelty, this approach seeks out a diverse set of solutions, each potentially offering unique advantages.

Building on the idea of novelty search, Quality Diversity (QD) optimization aims to find a collection of high-quality solutions that are also diverse.
The goal is not just to find the best solution but to map out the entire landscape of potential solutions, each excelling in different ways.
This approach provides a broader understanding of the problem space and uncovers a variety of viable solutions.

Take a robot controller as an example.
If you want the robot to be able to walk efficiently, you might define an objective as the distance covered over a set amount of time.
Optimizing towards this objective may give controllers that shuffle along, then walk, then run.
The first insight, from Novelty Search, is that the path from shuffling to running might not be straightforward; maybe the optimization process needs to first explore robot jumping before it can understand how to walk, and maybe skipping is a necessary stepping stone on the way to running.
The second insight, from QD, is that we don't just want a running robot.
If an actuator on the robot's right leg breaks, a skipping behavior is the most efficient.
If the robot is put on rugged terrain, jumping might be necessary.
If there's suddenly an overhead obstacle, the robot will need to duck.
So, if we optimize for running, we risk missing out on these other useful behaviors.
But if we optimize for a diversity of controllers related to running, we'll naturally build up a repertoire of high-quality behaviors.
QD builds in robustness through diversity.

## QD algorithms

Most QD algorithms, including the seminal [MAP-Elites algorithm](https://arxiv.org/pdf/1504.04909), follow the same steps. First, a behavior or feature space is defined, which will be used to store solutions. Each cell in this grid represents a different type of solution. This space can first be filled up with random solutions, putting each random solution into its corresponding bin. The first algorithmic step is to sample from this space, usually sampling multiple different solutions at once.

[![QD step 1](/images/qd1.gif)](/images/qd1.gif)

In the above image, which uses a video from the excellent [QDAC](https://adaptive-intelligent-robotics.github.io/QDAC/) article, an example behavior is sampled from the archive.
The archive could be organized based on the use of each leg, for example, so this controller would come from a corner representing high usage of one leg and low usage of another.
Most QD algorithms sample multiple solutions at once and do the following steps in parallel.

The next step is to modify the solution.
This can be done in a random way, like randomly changing a parameter in a model, but it can also be done in an informed way.
Methods like [PGA-ME](https://dl.acm.org/doi/pdf/10.1145/3449639.3459304?) use reinforcement learning to modify the solutions.
This modification step produces new solutions which may exhibit new behaviors.

[![QD step 2](/images/qd2.gif)](/images/qd2.gif)

The new solutions are then evaluated in whatever problem environment they're intended for.
This evaluation needs to return two pieces of information: how good the solution is (quality), and a description of how it worked (for diversity).
That information will be used to put it into the archive, where it will be compared to other similar solutions.

[![QD step 3](/images/qd3.gif)](/images/qd3.gif)

This process is then repeated, until a sufficient diversity is found, the process stops exploring, or the user running the process simply decides to end it.
Each iteration will select behaviors which will be modified, leading to more new behaviors, which will be added to the behavior space, and so on.
The goal is to cover this behavior space as much as possible using this iterative process.

[![QD step 4](/images/qd4.gif)](/images/qd4.gif)

MAP-Elites was developed in 2015 and since then, there have been [many improvements, modifications, and new QD algorithms](https://quality-diversity.github.io/papers) proposed.
These enhancements range from different methods of dividing the solution space to incorporating more sophisticated variation and selection techniques.
They are now used in robotics for developing diverse repertoires of behaviors, in engineering for generating varied aerodynamic shapes, and even in creative fields like video game design.
QD algorithms have also expanded beyond traditional evolutionary computation, using [gradient-based methods](https://proceedings.neurips.cc/paper/2021/file/532923f11ac97d3e7cb0130315b067dc-Paper.pdf) instead.
All of these QD methods share a similar philosophy, though, which is that a set of diverse solutions is better than a single one.

## The value of diversity

It is this underlying philosophy of QD — searching explicitly for a diversity of good solutions — that I want to highlight.
Many optimization methods, like those used in machine learning, often aim for a single model, but there’s great value in diversity.
For example, many different large language models have now been trained and made available.
Those models are somewhat diverse due to the different datasets and different architectures used.
This diversity has been helpful for model merging methods, which aggregate different models into one.
But this diversity wasn't intentional, just the result of different teams and companies doing a similar task.
Instead of letting this diversity arise spontaneously, why not explicitly seek it?

QD can enhance robustness and adaptability, providing a suite of solutions tailored to different scenarios rather than a one-size-fits-all solution.
By shifting our focus from finding a single best solution to exploring a diverse array of high-quality solutions, we open up new possibilities for innovation and problem-solving.
Whether in engineering, robotics, or machine learning, the search for a diverse set of solutions can be a more comprehensive and adaptable approach.
