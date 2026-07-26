---
title:          "Characterization-Guided GPU Fault Resilience in NVIDIA MPS"
date:           2026-05-16 19:22:28 +0000
selected:       true
# pub:            "International Conference on Learning Representations (ICLR)"
# pub_pre:        "Accepted by "
pub_post:       'Under review.'
# pub_last:       ' <span class="badge badge-pill badge-publication badge-success">Spotlight</span>'
pub_date:       "2026"
semantic_scholar_id: c4558605e964bbce4827e56b8b1cba620ad1e35b  # use this to retrieve citation count
abstract: >-
  NVIDIA Multi-Process Service (MPS) enables fine-grained GPU sharing by allowing multiple processes to execute concurrently on the same GPU, making it an important mechanism for improving GPU utilization. However, MPS has weak fault resilience: a fault in one process can terminate all co-running processes, limiting its adoption in resilience-critical settings such as multi-tenant GPU clusters. In this work, we design fault-resilient MPS to solve this problem. Our design is guided by insights from a systematic characterization of GPU faults and a deep analysis of their end-to-end processing pipeline. Based on these insights, we design two complementary mechanisms. A fault isolation mechanism for the dominant memory-related faults that can be fully isolated by software intervention in the open GPU driver kernel module. For other faults whose process is within proprietary software, we design a practical mechanism -- fast recovery using virtual memory based GPU-resident state sharing. Our evaluation on different GPUs and workloads shows that these mechanisms can handle corresponding faults effectively with minimal overhead.
cover:          /assets/images/covers/Fault-Resilient MPS.png
authors:
  - Rixin Liu
  - Xingqi Cui
  - Kaijian Wang
  - Xinheng Ding
  - Zirui Liu
  - Yuke Wang
  - Jiarong Xing
links:
    paper: https://arxiv.org/abs/2605.26461
    code: https://github.com/RixinLiu/Fault-Resilient-MPS
#   Unsplash: https://unsplash.com/photos/sliced-in-half-pineapple--_PLJZmHZzk
---
