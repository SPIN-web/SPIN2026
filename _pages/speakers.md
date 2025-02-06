---
layout: home
permalink: /speakers
order: 4
---

# Invited speakers

## Orna Grumberg (Technion, Israel)

![Orna Grumberg](assets/images/orna.jpg){:width="20%" style="float: left; margin-right: 12pt"}

### Developments in Symbolic Model Checking

**Abstract:** Model Checking is a powerful technique that, when provided with a software or hardware system and a specification, automatically determines whether the system meets its specification. Despite its successes, there are continuous efforts to find new methods and techniques that can broaden the scope of model checking to more complex systems and properties. One particularly appealing approach is symbolic model checking, which reformulates the issue into a logical representation and takes advantage of significant improvements in satisfiability solvers to tackle the model checking challenges.
Initially, hardware model checking has been translated into a propositional formula, with its satisfiability being evaluated by a SAT solver. Subsequently, software model checking was transformed into a first-order formula, to which an SMT solver was employed. Recently, Constrained Horn Clauses (CHC) have demonstrated effectiveness in proving program correctness with respect to safety properties.
In this presentation, we will introduce CHCs and demonstrate several non-standard CHC applications for problems beyond safety.

**Bio:** [Orna Grumberg](https://orna.cswp.cs.technion.ac.il/) is a Professor in the Computer Science Department at the Technion, Israel. She is a member of the Academia Europaea and an ACM Fellow. She earned her Ph.D. from the Technion's Computer Science Department and holds an Honorary Doctorate from the Technical University of Munich.
Her research interests include automated verification of software and hardware, automated program repair, leveraging model checking to identify security vulnerabilities, as well as abstraction, refinement, and modularity in model checking. She also focuses on automata-learning, temporal logics and automata on infinite objects.
Grumberg is a member of the steering committee for the premier conference on model checking, Computer-Aided Verification (CAV). She is the co-author of the widely cited book “Model Checking” and its second edition, “Model Checking - Second Edition.” Her contributions to CounterExample-Guided Abstraction Refinement (CEGAR) have earned her the CAV award.

## Alexandre Duret-Lutz: (EPITA Research Laboratory (LRE))

![Alexandre Duret-Lutz](assets/images/alexandre.jpg){:width="20%" style="float: left; margin-right: 12pt"}

### Growing an ω-automata library

**Abstract:** This is a talk about the past, present, and future of
[Spot](https://spot.lre.epita.fr/), a C++ library for the manipulation
of linear-time temporal logic and ω-automata, with applications to
model-checking and reactive synthesis.  Today, most of the features of
Spot revolve around its support for transition-based Emerson-Lei
automata.  I'll review key developments in the history of Spot, and give
an account of recently introduced features that I find exciting.

**Bio:** [Alexandre Duret-Lutz](https://www.lrde.epita.fr/~adl/) is a professor at Epita, working in the LRE, its research and development laboratory.
He has a habilitation (french HDR) from Université Pierre & Marie Curie (Paris 6).
His research is about omega-automata and their use in model checking. To support that, he develops SPOT, a C++ library for manipulation of omega-automata (with arbitrary acceptance condition) that also offers features necessary to implement model checkers.
Between 2007 and 2014, Alexandre was also participating to the Vaucanson (now renamed VCSN) project: a finite automata library.
