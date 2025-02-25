---
title: Recurrence-based time extrapolation
summary: Fast simulations of passive and weakly coupled transport processes in recurrent flows
date: 2025-02-21
type: article
math: false
featured: true

image:
  placement: 1
  caption: Distance plot of a fluidized bed. Bold, black lines indicate time intervals used for the time-extrapolated series. Dashed, black lines connect similar states, i.e. recurrences.
  focal_point: "Center"
  preview_only: false

---

Many driven, dissipative systems exhibit recurrent behavior, i.e., the same states appear again and again albeit in a completely irregular fashion. Examples include particulate flows like fluidized beds and rotating drums and other types of multiphase flow such as bubble columns. If slow, transient, long-term processes take place in such systems, one may decouple them from the fast, recurrent dynamics and use the following, simple approximation for the latter. 

First a time series of flow fields is recorded that contains recurrences of the volume fraction {{< math >}}$\alpha_{\textrm{g,p}}(\boldsymbol{r},t)${{< /math >}} and velocity fields {{< math >}}$\boldsymbol{u}_{\textrm{g,p}}(\boldsymbol{r},t)${{< /math >}}. In many cases, a few seconds are enough to characterize the ongoing dynamics.
Then the series is extrapolated with large time steps employing recurrence statistics. To predict how a state will evolve, the most similar one in the recorded time series is identified and its evolution is used. Upon iteration, one can create sequences {{< math >}}$\alpha_{\textrm{g,p}}^{\textrm{(rec)}}(\boldsymbol{r},t)${{< /math >}}, {{< math >}}$\boldsymbol{u}_{\textrm{g,p}}^{\textrm{(rec)}}(\boldsymbol{r},t)${{< /math >}} of almost arbitrary length to approximate the actual long-term dynamics. Such a series has the same statistical properties in terms of spatially resolved temporal averages and variances as the underlying, short time series. This provides a criterion on their required length.

Finally, one can carry out very fast simulations of transport processes on the time-extrapolated sequences. For the case of passive transport in the gas phase with an interaction term inline math {{< math >}}$S_{\textrm{p-g}}${{< /math >}} with a secondary, particulate one, one only has to solve

{{< math >}}
$$
\frac{\partial \alpha_{\textrm{g}}^{\textrm{(rec)}} c}{\partial t} + \nabla\cdot \alpha_{\textrm{g}}^{\textrm{(rec)}}\boldsymbol{u}_{\textrm{g}}^{\textrm{(rec)}}c = \nabla\cdot \alpha_{\textrm{g}}^{\textrm{(rec)}} D^{\textrm{(rec)}}\nabla c + S_{\textrm{p-g}}
$$
{{< /math >}}
without the need to compute the velocity and volume fraction fields. Similarly, the particle dynamics can be approximated based on their time-extrapolated velocity field {{< math >}}$\boldsymbol{u}^{\textrm{(rec)}}_{\textrm{p}}${{< /math >}}.
Such a simplified treatment led to speed ups between two and three orders of magnitude compared to the full calculations for transport of species and heat.


**References on recurrence statistics and recurrence CFD:**

<a href="https://doi.org/10.1016/j.ces.2022.117795"> T. Lichtenegger, S. Abbasi, and S. Pirker, Transport in turbulent, recurrent flows: Time-extrapolation and statistical symmetrization, Chem. Eng. Sci. 259 (2022) 117795. </a>

<a href="https://doi.org/10.1103/PhysRevFluids.6.044310"> F. Dabbagh et al., Disclosing recurrence properties in fluidized beds, Phys. Rev. Fluids 6 (4) (2021) 044310. </a>

<a href="https://doi.org/10.1063/5.0025597"> T. Lichtenegger and T. Miethlinger, On the connection between Lagrangian and Eulerian metrics for recurrent particulate flows, Phys. Fluids 32 (11) (2020) 113308. </a>

<a href="https://doi.org/10.1063/5.0010315">  S. Abbasi et al., Recurrence analysis and time extrapolation of a confined turbulent jet using modal decomposition, Phys. Fluids 32 (7) (2020) 075115. </a>

<a href="https://doi.org/10.1016/j.compfluid.2019.104348">  S. Abbasi, S. Pirker, and T. Lichtenegger, Application of recurrence CFD (rCFD) to species transport in turbulent vortex shedding, Comput. Fluids 196 (2020) 104348. </a>

<a href="https://doi.org/10.1016/j.ijmultiphaseflow.2018.05.013">  T. Lichtenegger, Local and global recurrences in dynamic gas-solid flows, Int. J. Multiph. Flow 106 (2018) 125-137.
</a>

<a href="https://doi.org/10.1016/j.cej.2019.01.161"> T. Lichtenegger et al., Dynamics and long-time behavior of gas–solid flows on recurrent-transient backgrounds, Chem. Eng. J. 364 (2019) 562–577. </a>

<a href="https://doi.org/10.1016/j.partic.2018.01.008"> P. Kieckhefen et al., Simulation of spray coating in a spouted bed using recurrence CFD, Particuology 42 (2019) 92–103. </a>

<a href="https://doi.org/10.1016/j.ces.2017.06.022"> T. Lichtenegger et al., A recurrence CFD study of heat transfer in a fluidized bed, Chem. Eng. Sci. 172 (2017) 310–322. </a>

<a href="https://doi.org/10.1016/j.ces.2016.07.036"> T. Lichtenegger and S. Pirker, Recurrence CFD - a novel approach to simulate multiphase flows with strongly separated time scales, Chem. Eng. Sci. 153 (2016) 394–410. </a>

<a href="https://doi.org/10.1209/0295-5075/4/9/004"> J.-P. Eckmann, S. O. Kamphorst, and D. Ruelle. Recurrence plots of dynamical systems. Europhys. Lett 4 (9) (1987) 973–977. </a>
