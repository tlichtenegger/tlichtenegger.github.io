---
title: "Transport in turbulent, recurrent flows: Time-extrapolation and statistical symmetrization"
authors:
- admin
- Sanaz Abbasi
- Stefan Pirker

date: "2022-02-23T00:00:00Z"
doi: "10.1016/j.ces.2022.117795"

# Schedule page publish date (NOT publication's date).
publishDate: "2022-02-23T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: "article"

# Publication name and optional abbreviated publication name.
publication: "Chemical Engineering Science"
publication_short: ""

abstract: We investigate bubble dynamics in a submerged double-jet as an example of weakly coupled, Lagrangian transport. The setup resembles continuous casting of steel at Reynolds numbers Re = 136 000 to Re = 272 000. Using short time series of flow fields obtained from large-eddy simulations (LES) with a discrete bubble model, we calculate a database of transport patterns and time-extrapolate them to long durations in the framework of recurrence CFD (rCFD). A dedicated averaging procedure along bubble trajectories allows us to study their transport with large steps at little numerical costs and monitor their spatial distribution. Besides time-extrapolation for fixed Re with a single database, we demonstrate how several time series can be combined to (i) enforce symmetries and (ii) approximately model conditions in between. We compare bubble volume fraction fields and total hold-up obtained from LES and from rCFD and find very good to satisfying agreement with speed up factors of more than 500.

# Summary. An optional shortened abstract.
summary:

tags:
- submerged double-jet, bubble transport, multi-scale problems, data-assisted simulations, time-extrapolation, recurrence CFD

featured: true

links:
- name: journal Link
  url: https://www.sciencedirect.com/science/article/pii/S0009250922003797
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

Together with my former PhD student Sanaz, I studied bubble transport in a strongly turbulent double-jet configuration and a data-assisted strategy to predict the long-term bubble distribution in the domain. Despite of massive fluctuations of the velocity field that hid any larger-scale recurrences of the flow topology, our nearest-neighbor-based approach recurrence CFD produced results in surprisingly good agreement with detailed LES data.
