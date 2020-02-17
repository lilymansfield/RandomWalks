# PHYS250 assignment 2: random walkers

### Introduction
For the first assingment, you evaluated multiple algorithms and generation parameters for random numbers and performed tests of those random numbers for uniformity and perhaps intrinsic randomness. The purpose of that assignment was to gain familiarity with basic (`python`) syntax, libraries, and functions, to practice using GitHub as a development tool for your software, and to begin to establish your own approach to programming for a specific purpose.

For your second assignment, we're going to elaborate on some of these skills, focus a bit more on quantitative analysis of important physical and emergent phenomena, and do a bit more plotting, graphing, and visualizing.

### Assignment Details
Specifically, I want you to use the random walker discussion and the examples (much of which is included in this repository as a starting point) to evaluate properties of random walks in more detail. We are going to connect this to the quintessential physics problem of Brownian motion, which was studied in detail by many people, including Einstein.


#### 1D random walk

Let's start by analyzing some features of a random walk in 1D. This is equivalent to the diffusion of a particle in 1D, or as someone mentioned in class, one approach to studying the stock market.

1. Plot the average and RMS displacement (total length of walk) for an ensemble of one-dimensional (1D) random walks each of which have `Nsteps = 100` and a constant stepsize. How many random walks do you need to simulate until you get a "good" measurement of the RMS displacement? How have you defined "good"?
1. Overlay the mean and RMS displacements for random walks of `Nsteps = 10^3, 10^4, and 10^6` on top of the one from the previous question.
1. Take two particles that are undergoing a 1D random walk and allow them each to undergo random walks of a fixed number of `Nsteps = N` with fixed length, as above. As a function of `N` determine the fraction of random walks where the two particles both end their walks at the origin (i.e. their total displacement is exactly equal to zero).  

#### 2D random walk

1. Plot the average and RMS displacement (total length of walk) for an ensemble of two-dimensional (2D) random walks each of which have `Nsteps = 100` and a constant stepsize. How many random walks do you need to simulate until you get a "good" measurement of the RMS displacement in 2D?
1. Measure the distribution of the magnitudes of the total displacement (i.e. the endpoints) of the random walks in 2D with a number of steps `Nsteps = 10^y` and `y = 0, 1, 2, 4, 6`.
1. Produce a scatter plot of the endpoints of 10000 random walks with `Nsteps = 1, 10`, superimposed on the same plot with large `Nsteps` (and justify what large means)
1. Write a routine that plots a histogram of the endpoints of `W` 2D random walks with `Nsteps` steps and 50 bins, along with the prediction given by a normal, or Gaussian, distribution for `x` in `(−3sigma, 3sigma)`, where `sigma=sqrt(Nsteps)xL` (where `L` is the fixed length of each step).
1. Do a histogram with `W = 10000` and `N = 1, 2, 3, 5`. How quickly does the Gaussian distribution become a good approximation to the random walk? How are you quanitfying "good"?
1. Compare your measurement to the expectation given by the Gaussian and compute a chi-squared. Assess how well your measurement matches the expectation.

*Optional*
1. Update the model to perform random walks that allow for a uniform direction in angle (i.e. not just `+/- 1` in `x,y`)
1. Extrapolate to 3D
1. Randomize the length of the steps taken.
1. Add an external *force* or a *field* that creates a preferred direction.

