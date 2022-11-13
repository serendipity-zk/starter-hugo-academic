---
title: 'Enabling Architectural Simulations and Optimizations of Production Web Services'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - Kan Zhu (First Author)
  - ......

# Author notes (optional)
# author_notes:
#   - 'Equal contribution'
#   - 'Equal contribution'

date: '2013-07-01T00:00:00Z'
doi: ''

# Schedule page publish date (NOT publication's date).
publishDate: '2017-01-01T00:00:00Z'

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ['1']

# Publication name and optional abbreviated publication name.
publication: In Submission to *ASPLOS*
publication_short: In Submission to *ASPLOS*

abstract: |2-
Modern web services are pervasive, running across hundreds
of thousands of servers in data centers. Hence, even
a small improvement in server efficiency can achieve significant
financial and environmental benefits. 

Improving server efficiency requires a comprehensive study of production web
services’ micro-architectural behaviors. To this end, we
design Ally, a simulation and characterization infrastructure
that enables studying production web services’ microarchitectural
behaviors using recently-released traces of
widely-used production Google applications. 

We identify and mitigate unique challenges in enabling micro-architectural
simulations of these traces via novel techniques introduced by
Ally. Apart from enabling meaningful research on improving
micro-architectural performance, Ally identifies open-source
applications that represent production behaviors.


Based on the simulation and characterization Ally enables,
we determine key micro-architectural performance bottlenecks
faced by production services, identifying several future optimization
opportunities. As examples, we identify that processors
must (1) handle massive thread oversubscription and
(2) utilize available bandwidth to manage large instruction
and data footprints. Based on our case studies of microarchitectural
optimizations, we evaluate context-driven thread
scheduling and bandwidth-aware hardware prefetching to
eliminate 5% and 28% of cache misses faced by these services.
Ally also motivates other future research directions,
such as reducing the warm-up time for predictors and caches.

# Summary. An optional shortened abstract.
summary: |2-
    * We proposed Ally, a novel simulation and characterization infrastructure that enables studying web services’ micro-architecture behaviors using Google applications
    * We identify the main bottleneck as thread oversubscription and low prefetch bandwidth usage

tags: []

# Display this page in the Featured widget?
featured: true

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

# url_pdf: ''
# url_code: 'https://github.com/wowchemy/wowchemy-hugo-themes'
# url_dataset: 'https://github.com/wowchemy/wowchemy-hugo-themes'
# url_poster: ''
# url_project: ''
# url_slides: ''
# url_source: 'https://github.com/wowchemy/wowchemy-hugo-themes'
# url_video: 'https://youtube.com'

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
image:
  caption: 'Data center'
  focal_point: ''
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
# projects:
#   - example

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
# slides: example
---

<!-- {{% callout note %}}
Click the _Cite_ button above to demo the feature to enable visitors to import publication metadata into their reference management software.
{{% /callout %}}

{{% callout note %}}
Create your slides in Markdown - click the _Slides_ button to check out the example.
{{% /callout %}}

Supplementary notes can be added here, including [code, math, and images](https://wowchemy.com/docs/writing-markdown-latex/). -->
