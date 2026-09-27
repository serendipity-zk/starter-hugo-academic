---
title: NanoFlow
summary: A throughput-oriented LLM serving framework that exploits intra-device parallelism, overlapping compute, memory, and network operations within a single GPU (OSDI 2025). Its asynchronous scheduling is adopted in SGLang, and similar overlapping designs now appear in most mainstream serving engines.
tags: [Research]
date: 2024-08-22
weight: 3
external_link: ""
url_code: https://github.com/efeslab/Nanoflow
url_pdf: https://arxiv.org/abs/2408.12757
links: []
image:
  caption: ''
  focal_point: Smart
---

NanoFlow is a throughput-oriented serving framework for large language models, published at OSDI 2025. End-to-end LLM serving is compute-bound for most common workloads, yet existing engines execute compute, memory, and network operations sequentially within a device. NanoFlow instead exploits intra-device parallelism: it splits inputs into nano-batches and overlaps these heterogeneous operations on a single GPU.

## Impact

NanoFlow's asynchronous scheduling, which prepares the next batch on the CPU while the GPU runs the current one, is integrated into [SGLang](https://www.lmsys.org/blog/2024-12-04-sglang-v0-4/) as its zero-overhead batch scheduler, enabled by default since SGLang v0.4. Similar ideas of overlapping CPU scheduling, computation, and communication are now part of most mainstream serving engines and systems, including [vLLM](https://github.com/vllm-project/vllm/releases/tag/v0.14.0) (async scheduling), [TensorRT-LLM](https://nvidia.github.io/TensorRT-LLM/features/overlap-scheduler.html) (overlap scheduler), and [TokenWeave](https://arxiv.org/abs/2505.11329) (compute–communication overlap).

The code is available on [GitHub](https://github.com/efeslab/Nanoflow).
