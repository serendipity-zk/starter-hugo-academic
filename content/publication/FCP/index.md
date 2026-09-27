---
title: 'Unleashing Scalable Context Parallelism for Foundation Models Pre-Training via FCP'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - Yilong Zhao
  - Xiaonan Nie
  - admin
  - Shuang Ma
  - Zhichao Lai
  - Hongxiang Hao
  - Yang Zhou
  - Baris Kasikci
  - Ion Stoica

bold_author: "Kan Zhu"

# Author notes (optional)
# author_notes:
#   - 'Equal contribution'
#   - 'Equal contribution'

date: '2026-05-18T00:00:00Z'
doi: ''
weight: 72
# Schedule page publish date (NOT publication's date).
# publishDate: '2017-01-01T00:00:00Z'

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ['1']

# Publication name and optional abbreviated publication name.
publication: MLSys 2026
publication_short: MLSys 2026

abstract: |
  Context parallelism (CP) has been widely adopted to support the growing context length in foundation model pretraining. However, existing designs fail to handle the large variation in sequence length from training datasets, resulting in suboptimal performance. These methods often over-shard short sequences, leading to compute inefficiency and excessive communication, or process long and short sequences separately without proper bin-packing, causing workload imbalance. In this paper, we propose FCP, a flexible context parallelism paradigm that shards and schedules sequences at block-level granularity. Instead of relying on rigid communication topologies such as ring, FCP enables arbitrary peer-to-peer communication, allowing flexible placement of sequence blocks across workers. By bin-packing blocks from both short and long sequences, FCP achieves both high compute efficiency and balanced workload distribution. Extensive evaluations show that FCP attains near-linear scalability on up to 256 NVIDIA GPUs, with 1.13x-2.21x improvement in the attention MFU.

tags: []

# Display this page in the Featured widget?
featured: false

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_pdf: 'https://arxiv.org/abs/2605.08524'
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
