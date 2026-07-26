---
title:          "Deterministic Inference Across Tensor Parallel Sizes That Eliminates Training-Inference Mismatch"
date:           2025-11-21 19:22:28 +0000
selected:       true
pub:            "International Conference on Machine Learning (ICML)"
# pub_pre:        "Accepted by "
# pub_post:       'Under review.'
# pub_last:       ' <span class="badge badge-pill badge-publication badge-success">Spotlight</span>'
pub_date:       "2026"
semantic_scholar_id: 025fd38dc51055f39f7d47aa8087cefad25e5af9  # use this to retrieve citation count
abstract: >-
  Deterministic inference is increasingly critical for large language model (LLM) applications such as LLM-asa-judge evaluation, multi-agent systems, and Reinforcement Learning (RL). However, existing LLM serving frameworks exhibit non-deterministic behavior: identical inputs can yield different outputs when system configurations (e.g., tensor parallel (TP) size, batch size) vary, even under greedy decoding. This arises from the non-associativity of floating-point arithmetic and inconsistent reduction orders across GPUs. While prior work has addressed batch-size–related nondeterminism through batch-invariant kernels, determinism across different TP sizes remains an open problem, particularly in RL settings, where the training engine typically uses Fully Sharded Data Parallel (i.e., TP = 1) while the rollout engine relies on multi-GPU TP to maximize the inference throughput, creating a natural mismatch between the two. This precision mismatch problem may lead to suboptimal performance or even collapse for RL training. We identify and analyze the root causes of TP-induced inconsistency and propose Tree-Based Invariant Kernels (TBIK), a set of TP-invariant matrix multiplication and reduction primitives that guarantee bit-wise identical results regardless of TP size. Our key insight is to align intra- and inter-GPU reduction orders through a unified hierarchical binary tree structure. We implement these kernels in Triton and integrate them into vLLM and FSDP. Experiments confirm zero probability divergence and bit-wise reproducibility for deterministic inference across different TP sizes. Also, we achieve bit-wise identical results between vLLM and FSDP in RL training pipelines with different parallel strategy.
cover:          /assets/images/covers/TBIK.png
authors:
  - Ziyang ZHang*
  - Xinheng Ding*
  - Jiayi Yuan
  - Rixin Liu
  - Huizi Mao
  - Jiarong Xing
  - Zirui Liu
links:
    paper: https://arxiv.org/pdf/2511.17826v1
    code: https://github.com/nanomaoli/llm_reproducibility
#   Unsplash: https://unsplash.com/photos/sliced-in-half-pineapple--_PLJZmHZzk
---
