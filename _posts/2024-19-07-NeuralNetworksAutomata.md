---
title: Neural Networks, Cellular Automata and Brain
date: 2024-07-19 11:06:00 +0800
categories: [Personal, Blog]
tags: [blog, math]     # TAG names should always be lowercase
math: true
---


## Introduction to Neural Networks and Cellular Automata

This post is an extract of a document/presentation i've made i'll illustrate only salient points of it. The full document is available [here](https://github.com/U-n-Own/UniversityNotes/blob/master/Assignments/ComputationalModelsComplexSystems/Presentation%20Notes/GrowingNeuralCellularAutomata-Slides.pdf).

### Neural Networks

Want to approximate a function from a $\mathcal{D}$ distribution $p(x,y)$ (data generating process)? Neural Networks are universal function approximators. 

In short compose a linear transformation $W$ over input space $X$ and apply a non-linear function $\sigma$ to it. Now repeat stacking layers $l$ and you have a "deep neural network". More units per layer $\rightarrow$ less layers needed. Just learn the linear transformation! 
In theory you can even learn the non-linearities [(KAN)](https://arxiv.org/html/2404.19756v1)

Micheal Nielsen's book [Neural Networks and Deep Learning](https://neuralnetworksanddeeplearning.com/) is a good starting point.


$$
\begin{aligned}
    y &= \sigma^l(W^lx + b^l) \\
\end{aligned}
$$

### Cellular Automata

Cellular Automata (CA) are biological inspired models of computation, their rich history cames from great minds like: Von Neumann, John Conway, Turing and many others.
When i say model of computation i mean we could theoretically build any computable function with these quite simple systems.

Basically, in the simplest setting you need a 2D grid of cells, but any dimension is possible. Then each of those cells can be in finite or continuous state space. And the dynamics of the system is given by the application in time of local rules.

$$
\begin{aligned}
    f_t: S^N \rightarrow S
\end{aligned} \\
\begin{aligned}
    f(cell_t) = f(cell_{t-1}, neighbours(cell_{t-1}))
\end{aligned}
$$

Where $f$ is the rule depending on the state of the cell and its neighbours. The most famous CA is Conway's Game of Life.

- *Rule 1*: Any live cell with fewer than two live neighbours dies, as if by underpopulation.
- *Rule 2*: Any live cell with two or three live neighbours lives on to the next generation.
- *Rule 3*: Any live cell with more than three live neighbours dies, as if by overpopulation.
- *Rule 4*: Any dead cell with exactly three live neighbours becomes a live cell, as if by reproduction.
- You can play it on: [Game of Life](https://playgameoflife.com/)


## Neural Cellular Automata

Every Neural guy want to parameterize something and then use neural net because it's cool. Since rules are function and state of grid can be seen as input, why do not use vectorized input and differentiable rules? We can backpropagate through the rules and learn them!

Of course it's more complex than that, but that's the idea. The paper [Growing Neural Cellular Automata](https://distill.pub/2020/growing-ca/) learn to grow and self-organize around a pattern or better a stable point (**attractor**).
$$
\begin{aligned}
    f_t: S^N \rightarrow S
\end{aligned} \\
\begin{aligned}
    f(cell_t) = \sigma(W^l \cdot cell_{t-1} + b^l)
\end{aligned}
$$

## Brain: System 1 and System 2

From the book [Thinking Fast and Slow](https://en.wikipedia.org/wiki/Thinking,_Fast_and_Slow) we get simple idea of dividing our brain in a fast taks solving system and a slow one for new task and complex problem.

- The System I is more intuitive, biased and lazy. It's the one we use when we have to walk, drive, talk about shit and so on...
- System II is more refined, comes to play when we have to do effortful thinking, learn a new skill or derive the KL-divergence.

### WiP...