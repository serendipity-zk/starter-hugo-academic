---
title: 'NanoFlow: Towards Optimal Large Language Model Serving Throughput'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - Kan Zhu
  - Yilong Zhao
  - Liangyu Zhao
  - Gefei Zuo
  - Yile Gu
  - Dedong Xie
  - Yufei Gao
  - Qinyu Xu
  - Tian Tang
  - Zihao Ye
  - Keisuke Kamahori
  - Chien-Yu Lin
  - Stephanie Wang
  - Arvind Krishnamurthy
  - Baris Kasikci

bold_author: "Kan Zhu"

# Author notes (optional)
# author_notes:
#   - 'Equal contribution'
#   - 'Equal contribution'

date: '2022-10-20T00:00:00Z'
doi: ''

# Schedule page publish date (NOT publication's date).
# publishDate: '2017-01-01T00:00:00Z'

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ['1']

# Publication name and optional abbreviated publication name.
publication: Arxiv 2024
publication_short: Arxiv 2024

abstract: |
  The increasing usage of Large Language Models (LLMs) has resulted in a surging demand for planet-scale serving systems, where tens of thousands of GPUs continuously serve hundreds of millions of users. Consequently, throughput (under reasonable latency constraints) has emerged as a key metric that determines serving systems' performance. To boost throughput, various methods of inter-device parallelism (e.g., data, tensor, pipeline) have been explored. However, existing methods do not consider overlapping the utilization of different resources within a single device, leading to underutilization and sub-optimal performance.

  We propose NanoFlow, a novel serving framework that exploits intra-device parallelism, which overlaps the usage of resources including compute, memory, and network within a single device through operation co-scheduling. To exploit intra-device parallelism, NanoFlow introduces two key innovations: First, NanoFlow splits requests into nano-batches at the granularity of operations, which breaks the dependency of sequential operations in LLM inference and enables overlapping; then, to get benefit from overlapping, NanoFlow uses an operation-level pipeline with execution unit scheduling, which partitions the device's functional units and simultaneously executes different operations in each unit. NanoFlow automates the pipeline setup using a parameter search algorithm, which enables easily porting NanoFlow to different models. We implement NanoFlow on NVIDIA GPUs and evaluate end-to-end serving throughput on several popular models such as LLaMA-2-70B, Mixtral 8x7B, LLaMA-3-8B, etc.. With practical workloads, NanoFlow provides 1.91x throughput boost compared to state-of-the-art serving systems achieving 59% to 72% of optimal throughput across ported models.


# Summary. An optional shortened abstract.
summary: |2-
    * Identified the underutilization of resources within a single device in existing serving systems due to sequentially executing operations with various resource requirements
    * Overlapping the utilization of different resources within a single device through operation co-scheduling for higher resource utilization
tags: []

# Display this page in the Featured widget?
featured: false

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
  caption: 'CPU'
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
