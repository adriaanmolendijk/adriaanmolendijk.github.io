---
title:  "Computability theory: an introduction"
layout: post
mathjax: true
---

In this post I will give a short introduction to the field of Computability theory.


I got acquainted with Computability theory during my Master degree at the [London School of Economics](https://www.lse.ac.uk/). There I wrote my dissertation on this exact topic, which can be found at one of the links at the bottom of the post.

# What is computability theory?

## The motivation

According to Wikipedia we have

That is, Computability theory is an academic field that falls within the broader theoretical computer science and mathematical philosophy. Computability theory tries to address the following questions:
- What does it mean for a function over the natural numbers to be computable?
- How can noncomputable functions be classified into a hierarchy based on their level of noncomputability?

I always like to compare these questions to the one(s) that are addressed by Computation theory ([https://en.wikipedia.org/wiki/Theory_of_computation](https://en.wikipedia.org/wiki/Theory_of_computation)). Computation theory tries to address the question
- Given a problem X, what are the resources needed to solve said problem?

As you can see, the questions are fundamentally different. While Computation theory really tries to understand the **resources** needed to solve a problem (often optimally), Computability theory tries to understand the fundamental limitations of what can be computed at all.

## The content

In this section I'll try to engage in a challenge and try to explain the basics of Computability theory. In fact, I'm aiming to sketch the argument that shows that there are functions that no computer in our universe can compute.

Let's get started. A Turing machine, due to Alan Turing, is a machine which has a paper tape of infinite length. The paper tape is split up into discrete cells, each cell containing a symbol from a fixed alphabet. The machine has a head which allows the machine to read, write and move along the tape, and the machine has an internal state which may change during the computation.

In this post we will not be concerned with the particular details of the Turing machine model. We will refer to a function $$f$$ as Turing computable or just computable if there is a Turing machine that, for each $$x$$ and $$y$$, terminates on input $$x$$ with output $$y$$ iff $$f(x) ≃ y$$. Simply put, a *function is computable if there is a Turing machine that computes it*.

Next, encoding. The coding of nonnumerical objects is fundamental for the theory of computability. The most important part of coding a set of objects is that we have an effective bijection between our set of objects and the natural numbers. An example of a set that can be coded into the natural numbers is the set $$\mathbb{N}$$, using the computable bijection 


$$⟨m,n⟩ = 12(m^2 + 2mn + n^2 + 3m + n).$$


The consequences of coding for the model of computability we presented earlier are as follows. For the Turing machine model, we can encode all the alphabet symbols and internal states, and from there encode all of the programs we can write on the machine as well. We obtain an effective enumeration of all functions we can compute using this model (for an explicit bijection between the set of all Turing programs and $$\mathbb{N}$$ see my dissertation).

Now comes the fun part. Fix such an enumeration by $\psi_0, \psi_1, \psi_2, \ldots$ and say that $$e$$ is an index of the computable function $$\psi_e$$ or index of the program $$Pe$$ (e.g. the $$e$$th Turing machine). This index is also called the *Godel number* for that program, named after Godel, who used the idea of coding formulas to prove his incompleteness theorem.


# Links
- [https://github.com/adriaanmolendijk/adriaanmolendijk.github.io/files/9173262/lse_master_dissertation.pdf](https://github.com/adriaanmolendijk/adriaanmolendijk.github.io/files/9173262/lse_master_dissertation.pdf)
- [https://en.wikipedia.org/wiki/Turing_machine](https://en.wikipedia.org/wiki/Turing_machine)
