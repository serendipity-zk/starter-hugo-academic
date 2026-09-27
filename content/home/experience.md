---
# An instance of the Experience widget.
# Documentation: https://wowchemy.com/docs/page-builder/
widget: experience

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 38

title: Experience
subtitle:
active: true
# Date format for experience
#   Refer to https://wowchemy.com/docs/customization/#date-format
date_format: Jan 2006

# Experiences.
#   Add/remove as many `experience` items below as you like.
#   Required fields are `title`, `company`, and `date_start`.
#   Leave `date_end` empty if it's your current employer.
#   Begin multi-line descriptions with YAML's `|2-` multi-line prefix.
experience:
  - title: Intern
    company: NVIDIA
    company_url: 'https://www.nvidia.com/'
    date_start: '2025-06-01'
    date_end: '2026-03-31'
    description: |2-
      * Enhanced the performance of Megatron-inference on Blackwell GPUs.
      * Improved the model weight resharding performance for Megatron-RL.

  - title: Intern
    company: ByteDance
    company_url: 'https://www.bytedance.com/'
    date_start: '2025-02-01'
    date_end: '2025-05-31'
    description: |2-
      * Explored efficient scheduling for mixed-SLO workloads in large-scale serving.

design:
  columns: '2'
---
