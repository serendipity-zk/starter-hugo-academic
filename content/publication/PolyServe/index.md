---
title: 'PolyServe: Efficient Multi-SLO Serving at Scale'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - admin
  - Haiyang Shi
  - Le Xu
  - Jiaxin Shan
  - Arvind Krishnamurthy
  - Baris Kasikci
  - Liguang Xie

bold_author: "Kan Zhu"

# Author notes (optional)
# author_notes:
#   - 'Equal contribution'
#   - 'Equal contribution'

date: '2025-07-17T00:00:00Z'
doi: ''
weight: 77
# Schedule page publish date (NOT publication's date).
# publishDate: '2017-01-01T00:00:00Z'

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ['3']

# Publication name and optional abbreviated publication name.
publication: arXiv 2025
publication_short: arXiv 2025

abstract: |
  Advances in Large Language Models (LLMs) have led to a surge of LLM-powered applications. These applications have diverse token-generation latency requirements. As a result, simply classifying workloads as latency-sensitive (LS) or best-effort (BE) overlooks the nuances within the latency-sensitive category and results in suboptimal user experiences and scheduling opportunities. However, efficiently serving requests with multiple SLO requirements poses significant challenges. First, all requests within a batch generate new tokens simultaneously, which can misalign them with their distinct SLO requirements. Moreover, while existing systems focus on auto-scaling for handling various overall request rates, the diversity of SLOs necessitates fine-grained auto-scaling among these SLO tiers. Finally, unlike LS/BE scenarios, where BE requests can be aborted at any time to ensure the SLO attainment of LS requests, those with different latency-sensitive SLOs cannot tolerate prolonged delays, and tail latency must be controlled.

  To tackle these challenges, we propose PolyServe, a novel multi-SLO scheduling policy at scale that maintains high SLO attainment while maximizing throughput. PolyServe first groups requests into multiple bins based on their per-token latency requirement, then schedules each bin to a subset of the server fleet. PolyServe routes requests to the highest-load but still SLO-attainable server to create a load gradient that facilitates auto-scaling. To increase utilization, PolyServe permits looser-SLO requests to share tighter-SLO instances when their own servers are saturated. PolyServe uses profiling data to guide scheduling decisions and manage tail latency through request-wait-time-aware scheduling, dynamic chunking, and continuous chunked prefill prediction. PolyServe achieves 1.23x goodput gain compared to existing policies, achieving up to 92.5% of optimal goodput.

summary: |2-
    * Grouped requests into bins by per-token latency requirement and scheduled each bin to a subset of servers
    * Maintained high SLO attainment while maximizing throughput for multi-SLO serving at scale
tags: []

# Display this page in the Featured widget?
featured: true

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_pdf: 'https://arxiv.org/abs/2507.17769'
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
