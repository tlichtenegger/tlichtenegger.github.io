---
title: Propagator formulation for transport processes
summary: Linear transport equations can be solved with large steps if the velocity field is known
date: 2025-02-20
type: article
math: false
featured: true

image:
  placement: 1
  caption: Propagator in the wake of a cylinder for two selected points (diamonds). Dashed lines represent the velocity field, round points the origin of influence for the diamonds. The ellipses indicate the width of the Gaussian approximation.
  focal_point: "Center"
  preview_only: false

---

For linear transport equations

{{< math >}}
$$
\frac{\partial c}{\partial t} + \nabla\cdot c\boldsymbol{u} = \nabla\cdot D\nabla c
$$
{{< /math >}}
of some concentration {{< math >}}$c(\boldsymbol{r}, t)${{< /math >}} (e.g., species or energy) subject to advection with a velocity field {{< math >}}$\boldsymbol{u}(\boldsymbol{r}, t)${{< /math >}} and diffusion with strength {{< math >}}$D(\boldsymbol{r}, t)${{< /math >}}, the future state after an arbitrarily long time step {{< math >}}$\Delta t_{\textrm{prop}}${{< /math >}}  needs to depend linearly on the field at {{< math >}}$t${{< /math >}}, i.e.,
{{< math >}}
$$
c(\boldsymbol{r}, t + \Delta t_{\textrm{prop}} ) = \int d^3r'  K_{\textrm{cc}} (\boldsymbol{r}, \boldsymbol{r}' ; \Delta t_{\textrm{prop}} , t) c(\boldsymbol{r}' , t).
$$
{{< /math >}}
{{< math >}}$K_{\textrm{cc}}${{< /math >}} is called the propagator of the transport equation and is itself a solution of this equation with initial condition {{< math >}}$K_{\textrm{cc}}(\boldsymbol{r}, \boldsymbol{r}' ; 0 , t) = \delta(\boldsymbol{r} - \boldsymbol{r}')${{< /math >}} for every {{< math >}}$\boldsymbol{r}'${{< /math >}}. For a mesh with {{< math >}}$N${{< /math >}} cells, one would have to solve {{< math >}}$N${{< /math >}} PDEs to compute the propagator and store a field with {{< math >}}$N^2${{< /math >}} values, which is computationally far too expensive. However, a much more efficient approximation is given by a shifted Gaussian
{{< math >}}
$$
K_{\textrm{cc}} (\boldsymbol{r}, \boldsymbol{r}' ; \Delta t_{\textrm{prop}} , t) \propto \textrm{e}^{-1/2\big(\boldsymbol{r}' - \boldsymbol{r}^{\textrm{(or)}}\big)\boldsymbol{\Sigma}^{-1}\big(\boldsymbol{r}' - \boldsymbol{r}^{\textrm{(or)}}\big)},
$$
{{< /math >}}
which can be calculated with little effort and does not require much memory.

For every point {{< math >}}$\boldsymbol{r}${{< /math >}} in the domain, this operator advects the concentration value from its origin {{< math >}}$\boldsymbol{r}^{\textrm{(or)}} (\boldsymbol{r}; \Delta t_{\textrm{prop}} , t)${{< /math >}} to {{< math >}}$\boldsymbol{r}${{< /math >}} and diffuse with strength {{< math >}}$\boldsymbol{\Sigma}(\boldsymbol{r}; \Delta t_{\textrm{prop}}, t)${{< /math >}} into an increasingly smeared out peak. Upon discretization, this amounts to cell-to-cell shifts with subsequent diffusion. Because very large time steps are permissible and the calculations are very simple, speed ups of several orders of magnitude compared to detailed CFD simulations are possible and brings us close to or even beyond real-time simulations.

Because this methodology relies on a priori knowledge of the velocity field, it is particularly suitable for recurrent flows (e.g., fluidized beds, bubble columns) or pseudosteady problems (e.g., moving beds).

**References on propagator transport simulations (transport-based recurrence CFD and pseudosteady CFD-DEM):**

<a href="https://doi.org/10.1103/PhysRevFluids.9.024401"> T. Lichtenegger. Data-assisted, physics-informed propagators for recurrent flows. Phys. Rev. Fluids 9.2 (2024) 024401. </a>

<a href="https://doi.org/10.1016/j.ces.2023.119402"> T. Lichtenegger and S. Pirker, Fast long-term simulations of hot, reacting, moving particle beds with a melting zone, Chem. Eng. Sci. 283 (2024) 119402. </a>

<a href="https://doi.org/10.1016/j.envsoft.2021.105172"> Y. Du et al. Efficient and high-resolution simulation of pollutant dispersion in complex urban environments by island-based recurrence CFD. Environ. Model. Softw. 145 (2021) 105172. </a>

<a href=" https://doi.org/10.1002/srin.202000214"> S. Pirker et al. Steel alloy homogenization during Rheinsahl–Heraeus vacuum treatment: conventional computational fluid dynamics, recurrence computational fluid dynamics, and plant observations. Steel Res. Int. 91.12 (2020) 2000214. </a>

<a href="https://doi.org/10.1016/j.ces.2018.09.043"> S. Pirker and T. Lichtenegger, Process control of through-flow reactor operation by real-time recurrence CFD (rCFD) simulations – proof of concept, Chem. Eng. Sci. 198 (2019) 241–252. </a>

<a href="https://doi.org/10.1016/j.ces.2018.04.059"> S. Pirker and T. Lichtenegger, Efficient time-extrapolation of single- and multiphase simulations by transport based recurrence CFD (rCFD), Chem. Eng.
Sci. 188 (2018) 65–83. </a>
