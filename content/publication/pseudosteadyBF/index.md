---
title: "Fast long-term simulations of hot, reacting, moving particle beds with a melting zone"
authors:
- admin
- Stefan Pirker

date: "2023-08-18T00:00:00Z"
doi: "10.1016/j.ces.2023.119402"

# Schedule page publish date (NOT publication's date).
publishDate: "2023-08-18T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: "article"

# Publication name and optional abbreviated publication name.
publication: "Chemical Engineering Science"
publication_short: ""

abstract: Hot, reacting, moving particle beds as found in blast furnaces comprise a wide range of spatial and temporal scales. We present an approach that combines models for granular motion, interfacial mass, momentum and heat transfer as well as heterogeneous multi-step reactions efficiently. Although they correspond to vastly different scales, long-term investigations built upon data from discrete-element simulations become feasible. The strategy was ﬁrst applied to 0.5 kg hematite reducing to iron under a CO atmosphere, where the most relevant reaction parameters were obtained from optimization towards experimental data. Then, we studied a 3D, full-scale blast furnace and its approach towards the thermo-chemical steady state over the course of 20 h. The framework may be easily extended, which will allow for realistic simulations of moving particle beds over process-relevant durations. It has the potential to create digital twins so that different reactor types can be optimized and novel designs explored.

# Summary. An optional shortened abstract.
summary:

tags:
- moving bed reactors, multiphysics flows, time-extrapolation

featured: true

links:
- name: journal Link
  url: https://www.sciencedirect.com/science/article/pii/S0009250923009582
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

Blast furnaces, still the dominant type of steel-making reactor, are diffiult to simulate because of the vastly different time scales involved. While stiff grains and fast gas flow dictate small time steps, large-scale material transport and chemical conversion take place over the course of hours. To bridge this massive gap, we employed a simple time-extrapolation technique built upon detailed CFD-DEM data from which we obtained the granular velocity field. To cover long durations, we replaced solid, interacting particles with non-interacting counterparts that followed the prescribed streamlines while exchanging heat and mass with the surrounding gas flow. This allowed us to use much larger time steps and describe the evolution of a full-scale blast furnace towards its thermo-chemical equilibrium at comparatively little numerical costs.
