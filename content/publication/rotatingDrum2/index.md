---
title: "Block-movement-based calibration of a discrete element model for fine, cohesive powders"
authors:
- Tobias Kronlachner
- Stefan Pirker
- admin

date: "2023-01-17T00:00:00Z"
doi: "10.1016/j.powtec.2023.118411"

# Schedule page publish date (NOT publication's date).
publishDate: "2023-01-17T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: "article"

# Publication name and optional abbreviated publication name.
publication: "Powder Technology"
publication_short: ""

abstract: Discrete-element-based simulations of highly cohesive powders require massive coarse-graining. Because corresponding material parameters are not known a priori, they need to be determined from calibration experiments with sufficient information content. We obtain these parameters for a highly and a mildly cohesive metal powder in a low-consolidated state such that they optimally reproduce lab-scale rotating-drum experiments with subsequent analysis of the material block structure. While standard discrete element models struggle to fully capture the dynamics, especially of highly cohesive powders, minimally invasive adaptions regarding rolling friction enable a very good agreement with experiments. Furthermore, we demonstrate that optimization based on characterization methods which provide less information might lead to multiple, different combinations of contact parameters (with some of them failing upon validation), whereas the block analysis produces a well-defined solution.

# Summary. An optional shortened abstract.
summary:

tags:
- cohesive powder, discrete element method, parameter optimization, rotating drum

featured: true

links:
- name: journal Link
  url: https://www.sciencedirect.com/science/article/pii/S003259102300195X
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

In this work, my former PhD student Tobias developed an optimization framework to obtain DEM parameters for highly cohesive powders from rotating drum experiments and subsequent block analysis. These parameters allowed for massively coarse-grained simulations in very good agreement with experiments.
