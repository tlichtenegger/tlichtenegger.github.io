---
title: "NeuralDEM - Real-time Simulation of Industrial Particulate Flows"
authors:
- Benedikt Alkin
- Tobias Kronlachner
- Samuele Papa
- Stefan Pirker
- admin
- Johannes Brandstetter

date: "2024-11-14T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2024-11-14T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["article"]

# Publication name and optional abbreviated publication name.
publication: "NeuralDEM - Real-time Simulation of Industrial Particulate Flows"
publication_short: ""

abstract: Advancements in computing power have made it possible to numerically simulate large-scale fluid-mechanical and/or particulate systems, many of which are integral to core industrial processes. Among the different numerical methods available, the discrete element method (DEM) provides one of the most accurate representations of a wide range of physical systems involving granular and discontinuous materials. Consequently, DEM has become a widely accepted approach for tackling engineering problems connected to granular flows and powder mechanics. Additionally, DEM can be integrated with grid-based computational fluid dynamics (CFD) methods, enabling the simulation of chemical processes taking place, e.g., in fluidized beds. However, DEM is computationally intensive because of the intrinsic multiscale nature of particulate systems, restricting simulation duration or number of particles. Towards this end, NeuralDEM presents an end-to-end approach to replace slow numerical DEM routines with fast, adaptable deep learning surrogates. NeuralDEM is capable of picturing long-term transport processes across different regimes using macroscopic observables without any reference to microscopic model parameters. First, NeuralDEM treats the Lagrangian discretization of DEM as an underlying continuous field, while simultaneously modeling macroscopic behavior directly as additional auxiliary fields. Second, NeuralDEM introduces multi-branch neural operators scalable to real-time modeling of industrially-sized scenarios - from slow and pseudo-steady to fast and transient. Such scenarios have previously posed insurmountable challenges for deep learning models. Notably, NeuralDEM faithfully models coupled CFD-DEM fluidized bed reactors of 160k CFD cells and 500k DEM particles for trajectories of 28s. NeuralDEM will open many new doors to advanced engineering and much faster process cycles. 

# Summary. An optional shortened abstract.
summary:

tags:
- universal physics transformers, real-time simulations, granular flows in various regimes

featured: true

links:
- name: arXiv Link
  url: https://arxiv.org/abs/2411.09678
url_pdf: https://arxiv.org/pdf/2411.09678
url_code: ''
url_dataset: ''
url_poster: ''
url_project: https://nx-ai.github.io/NeuralDEM/
url_slides: ''
url_source: ''
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: # 'Image credit: [**Unsplash**](https://unsplash.com/photos/s9CC2SKySJM)'
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects:
- internal-project

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: example
---

In this work, we let universal physics transformers learn the dynamics of granular matter both in the dense, pseudo-steady regime of hopper flow and the dilute, dynamic behavior encountered in fluidized bed reactors. The neural networks are trained with a large number of DEM and CFD-DEM trajectories for varying particle properties, boundary conditions and geometries. Long-term predictions for different values of these properties show (i) simulation speed ups of several orders of magnitude, (ii) very good generalization capabilities to unseen conditions, and (iii) the feasibility to directly use macroscopic material properties (e.g. angle of repose) instead of microscopic DEM parameters.
