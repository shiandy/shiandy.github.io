---
layout: default
title: Welcome
---

I am a senior at Harvard College, where I am a dual degree (AB/SM) candidate for
[statistics](http://stat.harvard.edu) and [Computational Science and Engineering
(CSE)](http://www.seas.harvard.edu/programs/graduate/computational-science-and-engineering/master-of-science-in-cse).
I'm currently a research assistant in the [Huttenhower
Lab](http://huttenhower.org/), where I build computational and statistical tools
to analyze microbiome data. I'm broadly interested in developing statistical
methods with applications in biology.

You can find me on [Github](https://github.com/shiandy),
[Bitbucket](https://bitbucket.org/andys314), or
[Linkedin](https://www.linkedin.com/in/andy-shi-b59550110).

<!---
<div style="text-align: center">
<a href="https://github.com/shiandy">Github</a> &bull;
<a href="https://bitbucket.org/andys314">Bitbucket</a> &bull;
<a href="https://www.linkedin.com/in/andy-shi-b59550110">Linkedin</a>
</div>
-->

## Education

+ **Harvard School of Engineering and Applied Sciences**, Cambridge, MA
(2015&ndash;2016) <br>
S.M. Degree Candidate in Computational Science and Engineering (CSE)

+ **Harvard College**, Cambridge, MA (2012&ndash;2016) <br>
A.B. Degree Candidate in Statistics. GPA: 3.84/4.0

## Publications/Projects

### Research Projects In Progress

+ Yasuda K, Gallini CA, **Shi A**, DuLong C, Schwager R, Hsu T, Abu-Ali G,
  Mclver L, Garrett WS, Huttenhower C, Morgan XC. Early life fluoride exposure
  affect the oral and gut microbiome in mice. *In preparation*.<br>
  R package for visualizing microbiome compositional data
  [[code](https://bitbucket.org/biobakery/mpuri)]

+ **Shi A**, Kostic AD, Schwager R, McIver L, Morgan XC, Huttenhower C.
  KneadData: Automated Quality Control and Filtering for High Throughput
  Sequencing Data. *In preparation*.
  [[homepage](http://huttenhower.org/kneaddata) |
  [code](https://bitbucket.org/biobakery/kneaddata)]

+ **Shi A**, Schwager E, Huttenhower C. Developing Power Calculations for
  Microbiome Compositional Data. *In progress*.
  [[progress report]({{ site.path }}/assets/power-calc-report.pdf) |
  [code](https://bitbucket.org/andys314/power-calculations)]

### Final Projects for Classes I Took

+ **A Graph Parallel Implementation of Hidden Markov Models**, with Kevin Schmid
  and Ding Zhou. *For CS 205: Computing Foundations for Computational Science
  (Spring 2015)*.
  <br>
  <small>
  Hidden Markov models (HMM) are often used to model time-series data for both
  discrete and continuous data. HMM has been successfully applied to problems
  such as speech recognition and gesture recognition. The parameters to a hidden
  Markov models are most commonly learned from the Baum-Welch&mdash;an
  Expectation Maximization (EM) algorithm. Unfortunately, the Baum-Welch
  algorithm is quadratic in number of states. A parallel implementation of the
  EM algorithm along the state axis would greatly improve scalability. Graph
  based platforms are particularly suited to EM algorithms, and our project uses
  GraphLab, a platform created by Dato for implementing graph based
  parallelizing schemes.
  </small>
  [[report](https://github.com/cs205-project-group/hmm/blob/master/paper/report.pdf) | [code](https://github.com/cs205-project-group/hmm)]

+ **The Impact of Education on Income**, with Diana Zhu. *For Stat 186: Causal
  Inference (Spring 2015)*. <br>
  <small>
  The relationship between education and income has long been a topic of
  interest among economists and education has been widely perceived as an
  effective way of reducing income inequality. Our project seeks to investigate
  their relationship using a cross-sectional dataset.
  </small>
  [[report](https://github.com/giraffe-186/education-income/blob/master/writeup_final.pdf)
  | [code](https://github.com/giraffe-186/education-income)]

+ **A Night at the Oscars**, with Antonio Coppola. *For AC 209: Data Science
  (Fall 2014)*. <br>
  <small>
  The relationship between education and income has long been a topic of
  In this project, we aim to discover which movie features (budget, director,
  review statistics, etc...) are predictive of success on the night of the
  Academy Awards, and to see how well a classifier can predict Oscar nominations
  and Oscar winnings.
  </small>
  [[webpage](http://coppola-shi.github.io/OscarNights/) |
  [code](https://github.com/coppola-shi/OscarNights)]

+ **Explorations to Optimize the Parareal Algorithm to Solve ODEs in Given
  Applications**, with Wesley Chen and Brandon Sim. *For AM 205: Advanced
  Scientific Computing: Numerical Methods (Fall 2014)*. <br>
  <small>
  The relationship between education and income has long been a topic of
  We look to achieve strong scaling in parallelizing numerical ODE methods. We
  test both parallelism by result space as well as parallelism by time, with the
  Parareal algorithm, to solve various ODEs. We measure performance and compare
  in terms of accuracy, speedup and efficiency. We provide some theoretical
  analysis for the Parareal algorithm’s runtime, speedup, error convergence, and
  stability. For the Parareal algorithm, we observe preliminary promising but
  not convincing results in our small scale tests up to 32 processors on
  Harvard’s Odyssey computing cluster. We analyze possible reasons as to why our
  implementation may not be ideal and some tradeoffs that are taken in the
  Parareal implementation. Further optimizations are proposed and rationalized
  as next steps including ports of to C++ using BLAS. Our code is written in
  Python using mpi4py. We compare tests from various data sources from basic
  exponential ODEs to larger grids of ODEs to solve for in applications like
  sound wave propagation.
  </small>
  [[report]({{ site.path }}/assets/parareal-paper.pdf) |
  [code](https://github.com/am205-project/parareal)]

+ **Pacman Agent**, with Kewei Li and Ding Zhou. *For CS 181: Machine Learning
  (Spring 2014)*. <br>
  <small>
  Implementation of an intelligent Pacman agent. We used both reinforcement
  learning and heuristics to train the agent. We also needed to classify
  capsules as real/placebo and ghosts by their "juiciness," using noisy
  observations.
  </small>
  [[report] ({{ site.path }}/assets/cs181_final_project_writeup.pdf) |
  [code](https://github.com/KDA9000/cs181_final_project)]

+ **OCaml Matrix**, with Luis Perez, Ding Zhou, and Zihao Wang. *For CS 51:
  Introduction to Computer Science II (Spring 2013)*. <br>
  <small>
  Implementation of a matrix module and the simplex algorithm, in OCaml.
  </small> <br>
  [[report]({{ site.path }}/assets/ocaml-matrix-report.pdf) |
  [draft spec]({{ site.path }}/assets/DraftSpec_Annotated.pdf) |
  [final spec]({{ site.path }}/assets/FinalSpec_Annotated.pdf) |
  [code](https://github.com/Fantastic-Four/ocaml-matrix)]


## Teaching

+ Teaching Fellow for Stat 102: Introduction to Statistics for Life Sciences
  (Spring 2016)
+ Teaching Fellow for [CS 109](http://cs109.org): Data Science (Fall 2015)
