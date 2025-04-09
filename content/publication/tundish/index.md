---
title: "Propagator-moments approximation for recurrence CFD: application to species transport in turbulent flows"
authors:
- Hannes Lumetzberger
- Stefan Pirker
- admin

date: "2025-04-04T00:00:00Z"
doi: "10.1016/j.ces.2025.121624"

# Schedule page publish date (NOT publication's date).
publishDate: "2025-04-04T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: "article"

# Publication name and optional abbreviated publication name.
publication: "Propagator-moments approximation for recurrence CFD: application to species transport in turbulent flows"
publication_short: ""

abstract: Accurate, long-term simulations of turbulent flows pose a large challenge for standard CFD algorithms. Recurrence CFD (rCFD) provides a simple, data-assisted approximation for recurrent dynamics. We present the theoretcal foundations of this approach in terms of propagator theory for passive transport processes and derive expressions for convective and diffusive contributions to large-step species transfer. We tested our new implementation on a double-sided, cuboid lid-driven cavity and compared various treatments of diffusion against detailed CFD calculations. Based on these insights, we applied the methodology to a down-scaled, industrial case of impurity transport in a steelmaking tundish at Reynolds number Re = 220 000. We obtained results in mostly very good agreement with detached-eddy simulations at 1/2700 of their runtime, which made rCFD faster than real time.

# Summary. An optional shortened abstract.
summary:

tags:
- time extrapolation, recurrence CFD, propagator formulation, turbulent species transport

featured: true

links:
- name: journal Link
  url: https://www.sciencedirect.com/science/article/pii/S0009250925004476
url_pdf: ''
url_code: ''
url_dataset: ''
url_poster: ''
url_project: ''
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

In his first paper, my PhD student Hannes employed the <a href="https://journals.aps.org/prfluids/abstract/10.1103/PhysRevFluids.9.024401"> propagator formalism</a> to establish a theoretical framework for transport-based recurrence CFD. Not only can we simulate transport processes, e.g., in turbulent flows faster than real time, now we also understand why. In the course of these theoretical developments, Hannes managed to determine a correction term for numerical diffusion in rCFD which makes simulation results also more accurate than those in our previous studies.
