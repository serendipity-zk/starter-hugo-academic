---
title: 'From Optimal to Practical: Efficient Micro-op Cache Replacement Policies for Data Center Applications'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - ......
  - "**Kan Zhu**"
  - Yilong Zhao
  - Yufei Gao
  - Peter Braun
  - Tanvir Ahmed Khan
  - Heiner Litz
  - Baris Kasikci
  - Shuwen Deng
  - ......

# Author notes (optional)
# author_notes:
#   - 'Equal contribution'
#   - 'Equal contribution'

date: '2024-10-20T00:00:00Z'
doi: ''
weight: 83
# Schedule page publish date (NOT publication's date).
# publishDate: '2017-01-01T00:00:00Z'

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ['1']

# Publication name and optional abbreviated publication name.
publication: International Symposium on High-Performance Computer Architecture (HPCA) 2025
publication_short: HPCA 2025


abstract: |
  Optimizing the CPU frontend has become crucial for modern processors with intricate instruction decoding logic, especially for efficiently running planet-scale data center applications. Micro-operation (micro-op) cache is a key unit to help improve the energy efficiency of the CPU frontend. Unfortunately, we find that data center applications suffer from frequent micro-op cache misses due to the lack of an effective micro-op cache replacement policy. Developing micro-op cache-specific replacement policies is challenging, as there currently does not exist an optimal theoretical solution akin to Belady’s algorithm for conventional caches. As a result, it is unknown by how much replacement policies can be improved and how to get there.

  To address these challenges, we introduce FLACK, a new near-optimal offline policy that considers the key features of the micro-op cache, such as variable and disproportional costs of micro-op cache misses and partial hits. We show that FLACK substantially outperforms Belady’s algorithm, thus establishing a new baseline for micro-op cache replacement policies. We then design FURBYS, a practical policy that mimics FLACK via profile-guided methods. FURBYS has three key components to perform cache replacement decisions: (1) it uses profiles of the whole-execution hit/miss behavior, (2) it detects locally (transiently) hot data, and (3) it selectively ignores data with profiled low hit rates.

  We evaluate FLACK and FURBYS using 11 data center applications and find that FLACK demonstrates an average bound of 30.21% miss reduction, achieving 4.46% greater miss reduction than Belady’s algorithm. Our practical policy, FURBYS, provides 14.34% average miss reduction compared to LRU, which is 1.84× greater than the current state-of-the-art replacement policy, contributing to 3.10% of performance-per-watt improvement for the CPU core. On average, in terms of miss reduction and IPC gain, FURBYS is equivalent to LRU policy on 1.5× micro-op cache sizes (up to 2×), demonstrating the effectiveness of the proposed replacement policy.


# Summary. An optional shortened abstract.
summary: |2-
    * Understand the limitations of state-of-the-art replacement policy and the uniqueness of micro-op cache.
    * Proposed and evaluated counter-based, profile-guided replacement policy
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
