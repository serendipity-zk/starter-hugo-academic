---
title: 'Themis: Software-Defined Hardware Prefetching'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - Keisuke Kamahori
  - Neil Adit
  - admin
  - Yuqi Mai
  - Victor Lee
  - Heiner Litz
  - Chris Kennelly
  - Snehasish Kumar
  - Hanna Alam
  - Milad Hashemi
  - David Li
  - Adrian Sampson
  - Baris Kasikci
  - Tipp Moseley
  - Parthasarathy Ranganathan
  - Akanksha Jain

bold_author: "Kan Zhu"

# Author notes (optional)
# author_notes:
#   - 'Equal contribution'
#   - 'Equal contribution'

date: '2026-07-31T00:00:00Z'
doi: ''
weight: 70
# Schedule page publish date (NOT publication's date).
# publishDate: '2017-01-01T00:00:00Z'

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ['3']

# Publication name and optional abbreviated publication name.
publication: arXiv 2026
publication_short: arXiv 2026

abstract: |
  Data cache misses represent a significant portion of stall cycles in datacenter workloads. Hardware prefetchers that reduce such stalls by fetching data ahead of time have become increasingly sophisticated. However, to achieve high coverage, they have to prefetch aggressively, generating many inaccurate accesses that waste memory bandwidth. This is problematic in datacenter environments where memory bandwidth is a limited resource due to high multi-tenancy. We observe that for datacenter workloads, inaccurate prefetches can be effectively filtered on a data page granularity, without sacrificing prefetch coverage. However, storing per-page metadata about prefetch usefulness in hardware is costly, so we propose a novel hardware-software interface for data prefetching: The software directs the hardware on where to prefetch, and the hardware identifies and issues prefetches in the regions of interest. We propose Themis, a profile-guided hardware prefetching solution that implements this new interface. Themis utilizes page-level hints stored in page-table entries to disable the prefetcher for certain data pages at runtime. Themis requires no binary or ISA changes and can be used to optimize processes without disrupting their execution. Themis is also orthogonal to existing works on prefetching and can be applied to optimize any hardware prefetcher. Our results show that Themis is able to achieve around 40% reduction in useless prefetch requests, resulting in speedup for all the evaluated prefetchers for datacenter workloads, including 4.1% for BOP, 3.1% for SPP+PPF, and 1.4% for Pythia.

tags: []

# Display this page in the Featured widget?
featured: false

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_pdf: 'https://arxiv.org/abs/2608.00259'
# url_code: ''
# url_dataset: ''
# url_poster: ''
# url_project: ''
# url_slides: ''
# url_source: ''
# url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
image:
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
