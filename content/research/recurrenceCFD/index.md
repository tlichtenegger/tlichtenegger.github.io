---
title: Recurrence-based time extrapolation
summary: Fast simulation of passive and weakly coupled transported processes in recurrent flows
date: 2025-02-21
type: article
math: false
featured: true

image:
  caption: Distance plot of a fluidized bed. Straight, black lines indicate time intervals used for the time-extrapolated series. Dashed, black lines represent the location of similar states at different times, i.e. recurrences.
  focal_point: ""
  preview_only: false

---

Many driven, dissipative systems exhibit recurrent behavior, i.e., the same states appear again and again albeit in a completely irregular fashion. Examples include particulate flows like fluidized beds and rotating drums. If slow, transient, long-term processes take place in such systems, one may decouple them from the fast, recurrent dynamics and use the following, simple approximation for the latter. 

First a time series of flow fields is recorded that contains recurrences of the volume fraction $\alpha\st{g,p}(\bvec{r},t)$ and velocity fields $\bvec{u}\st{g,p}(\bvec{r},t)$. In many cases, a few seconds are enough to characterize the ongoing dynamics.
Then the series is extrapolated with large time steps employing recurrence statistics~\cite{Eckmann1987}. To predict how a state will evolve, the most similar one in the recorded time series is identified and its evolution is used. Upon iteration, one can create sequences $\alpha\st{g,p}\spt{(rec)}(\bvec{r},t)$, $\bvec{u}\st{g,p}\spt{(rec)}(\bvec{r},t)$ of almost arbitrary length to approximate the actual long-term dynamics. Such a series has the same statistical properties in terms of spatially resolved temporal averages and variances as the underlying, short time series~\cite{Lichtenegger2022}. This provides a criterion on their required length.

Finally, one can carry out very fast simulations of transport processes on the time-extrapolated sequences. For the case of passive transport in the gas phase with an interaction term $S\st{p-g}$ with a secondary, particulate one, one only has to solve
\begin{align}
&\frac{\partial \alpha\st{g}\spt{(rec)} c}{\partial t} + \nabla\cdot \alpha\st{g}\spt{(rec)}\bvec{u}\st{g}\spt{(rec)}c = \nabla\cdot \alpha\st{g}\spt{(rec)} D\spt{(rec)}\nabla c + S\st{p-g}
\end{align}
without the need to compute the velocity and volume fraction fields. Similarly, the particle dynamics can be approximated based on their time-extrapolated velocity field $\uvec\spt{(rec)}\st{p}$ (cf.~Eq.~\eqref{eq:modelB}).
Such a simplified treatment led to speed ups between two and three orders of magnitude compared to the full calculations for transport of species~\cite{Abbasi2020a,Lichtenegger2022} and heat~\cite{Lichtenegger2017,Lichtenegger2019}.


**References on recurrence statistics and recurrence CFD:**

<a href="https://doi.org/10.1209/0295-5075/4/9/004"> J.-P. Eckmann, S. O. Kamphorst, and D. Ruelle. Recurrence plots of dynamical systems. Europhys. Lett 4 (9) (1987) 973–977. </a>

<a href="https://doi.org/10.1016/j.ces.2016.07.036"> T. Lichtenegger and S. Pirker, Recurrence CFD - a novel approach to simulate multiphase flows with strongly separated time scales, Chem. Eng. Sci. 153 (2016) 394–410. </a>

<a href="https://doi.org/10.1016/j.ces.2017.06.022"> T. Lichtenegger et al., A recurrence CFD study of heat transfer in a fluidized bed, Chem. Eng. Sci. 172 (2017) 310–322. </a>

<a href="https://doi.org/10.1016/j.partic.2018.01.008"> P. Kieckhefen et al., Simulation of spray coating in a spouted bed using recurrence CFD, Particuology 42 (2019) 92–103. </a>

<a href="https://doi.org/10.1016/j.cej.2019.01.161"> T. Lichtenegger et al., Dynamics and long-time behavior of gas–solid flows on recurrent-transient backgrounds, Chem. Eng. J. 364 (2019) 562–577. </a>

<a href="https://doi.org/">  </a>
