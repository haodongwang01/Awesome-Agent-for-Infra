# Agent for Operators, Kernels and Compilers

[Back to README](../README.md)

## Core Problem

Can agents generate, repair, and optimize the low-level code that determines real model performance?

This track covers CUDA, Triton, tensor programs, compiler schedules, graph rewrites, MLIR/LLVM-style transformations, and profiling-guided optimization. The central challenge is to make agents improve speed without breaking numerical contracts, portability, or maintainability.


## Key Questions

- Can an agent produce kernels that are both correct and faster than framework baselines?
- Can it use profiler traces, compiler errors, occupancy reports, and memory-access patterns as feedback?
- Can generated optimizations transfer across GPUs, CPUs, accelerators, and problem sizes?
- Can agents reason over compiler IRs and schedule spaces rather than only source code?

## Paper

This section is organized by the role each paper plays in the agent-for-kernels stack: benchmarks, trained kernel-generation agents, reusable optimization frameworks, and LLM-agent algorithm-discovery precedents.

### Benchmarks and Evaluation

| Date | Name | Title | Paper / Docs | Code |
|:-:|:-:|:-|:-:|:-:|
| 2026 May | `FastKernels` | Benchmarking GPU kernel generation in production serving workloads | [![Paper][paper-badge]](https://arxiv.org/abs/2605.23215) | [![Code][code-badge]](https://github.com/Snowflake-AI-Research/fastkernels) |
| 2026 May | `KernelBenchX` | Comprehensive category-aware benchmark for evaluating LLM-generated GPU kernels | [![Paper][paper-badge]](https://arxiv.org/abs/2605.04956) | [![Code][code-badge]](https://github.com/BonnieW05/KernelBenchX) |
| 2025 Jul | `GEAK` | Triton kernel AI agent and evaluation benchmarks for optimized GPU kernels | [![Paper][paper-badge]](https://arxiv.org/abs/2507.23194) | - |
| 2025 Feb | `KernelBench` | Benchmark for testing whether LLMs can write correct and faster GPU kernels | [![Paper][paper-badge]](https://arxiv.org/abs/2502.10517) | [![Code][code-badge]](https://github.com/ZichenZhu/KernelBench_Research) |

### Trained Kernel-Generation Agents

| Date | Name | Title | Paper / Docs | Code |
|:-:|:-:|:-|:-:|:-:|
| 2026 Jun | `daVinci-kernel` | Co-evolving skill selection, summarization, and utilization via RL for GPU kernel optimization | [![Paper][paper-badge]](https://arxiv.org/abs/2606.16497) | - |
| 2026 Jun | `MusaCoder` | Native GPU kernel generation with full-stack training on Moore Threads GPU | [![Paper][paper-badge]](https://arxiv.org/abs/2606.04847) | - |
| 2026 Mar | `DRTriton` | Large-scale synthetic data-driven reinforcement learning for Triton kernel generation | [![Paper][paper-badge]](https://arxiv.org/abs/2603.21465) | - |
| 2026 Feb | `Fine-Tuning GPT-5` | Fine-tuning GPT-5 for GPU kernel generation in Makora's training environment | [![Paper][paper-badge]](https://arxiv.org/abs/2602.11000) | - |
| 2026 Feb | `Dr. Kernel` | Reinforcement learning done right for Triton kernel generations | [![Paper][paper-badge]](https://arxiv.org/abs/2602.05885) | [![Code][code-badge]](https://github.com/hkust-nlp/KernelGYM) |
| 2025 Oct | `TritonRL` | Training LLMs to think and code Triton without cheating | [![Paper][paper-badge]](https://arxiv.org/abs/2510.17891) | - |
| 2025 Oct | `ConCuR` | Conciseness-oriented training data and KernelCoder for state-of-the-art kernel generation | [![Paper][paper-badge]](https://arxiv.org/abs/2510.07356) | - |
| 2025 Jul | `CUDA-L1` | Improving CUDA optimization via contrastive reinforcement learning | [![Paper][paper-badge]](https://arxiv.org/abs/2507.14111) [![Docs][docs-badge]](https://deepreinforce-ai.github.io/cudal1_blog) | - |

### Agentic Kernel Optimization Frameworks

| Date | Name | Title | Paper / Docs | Code |
|:-:|:-:|:-|:-:|:-:|
| 2026 Jun | `KForge` | LLM-driven cross-platform kernel generation for AI accelerators | [![Paper][paper-badge]](https://arxiv.org/abs/2606.02963) | - |
| 2026 Mar | `StitchCUDA` | Automated multi-agent end-to-end GPU programming with rubric-based agentic reinforcement learning | [![Paper][paper-badge]](https://arxiv.org/abs/2603.02637) | - |
| 2026 Mar | `KernelFoundry` | Hardware-aware evolutionary GPU kernel optimization with distributed benchmarking | [![Paper][paper-badge]](https://arxiv.org/abs/2603.12440) | - |
| 2026 Mar | `KernelSkill` | Multi-agent GPU kernel optimization with reusable expert skills and trajectory memory | [![Paper][paper-badge]](https://arxiv.org/abs/2603.10085) | [![Code][code-badge]](https://github.com/0satan0/KernelMem) |
| 2026 Jan | `Two-Stage GPU Kernel Tuner` | Semantic refactoring plus search-based optimization for GPU kernel tuning | [![Paper][paper-badge]](https://arxiv.org/abs/2601.12698) | - |
| 2025 Dec | `KernelEvolve` | Scaling agentic kernel coding for heterogeneous AI accelerators at Meta | [![Paper][paper-badge]](https://arxiv.org/abs/2512.23236) | - |
| 2025 Dec | `cuPilot` | Strategy-coordinated multi-agent framework for CUDA kernel evolution | [![Paper][paper-badge]](https://arxiv.org/abs/2512.16465) | [![Code][code-badge]](https://github.com/champloo2878/cuPilot-Kernels) |
| 2025 Nov | `CudaForge` | Agent framework with hardware feedback for CUDA kernel optimization | [![Paper][paper-badge]](https://arxiv.org/abs/2511.01884) | [![Code][code-badge]](https://github.com/OptimAI-Lab/CudaForge) |
| 2025 Oct | `STARK` | Strategic team of agents for refining kernels with profiling feedback | [![Paper][paper-badge]](https://arxiv.org/abs/2510.16996) | - |

### LLM-Agent Algorithm-Discovery Precedents

| Date | Name | Title | Paper / Docs | Code |
|:-:|:-:|:-|:-:|:-:|
| 2025 Jun | `AlphaEvolve` | Coding agent for scientific and algorithmic discovery | [![Paper][paper-badge]](https://arxiv.org/abs/2506.13131) | - |
| 2024 Jan | `Evolution of Heuristics` | Automatic algorithm design with large language models | [![Paper][paper-badge]](https://arxiv.org/abs/2401.02051) | [![Code][code-badge]](https://github.com/FeiLiu36/EoH) |
| 2023 Dec | `FunSearch` | Mathematical discoveries from program search with large language models | [![Paper][paper-badge]](https://www.nature.com/articles/s41586-023-06924-6) | [![Code][code-badge]](https://github.com/google-deepmind/funsearch) |

## Skills

| Skill | What it should do |
| --- | --- |
| `torch-to-triton` | Translate PyTorch reference ops into Triton candidates with correctness tests. |
| `cuda-compile-fix` | Repair CUDA/Triton compile failures with minimal semantic drift. |
| `profile-guided-kernel-tune` | Use Nsight, ncu, torch profiler, or benchmark traces to guide changes. |
| `numerics-guard` | Preserve dtype, tolerance, broadcasting, and edge-case contracts. |
| `compiler-pass-agent` | Propose and validate graph rewrites or IR transformations under tests. |
| `autotuning-budget-manager` | Allocate benchmark trials across candidate kernels, schedules, and hardware targets. |

## Toolchain

| Date | Name | Title | Paper / Docs | Code |
|:-:|:-:|:-|:-:|:-:|
| 2019 Jun | `Triton` | Intermediate language and compiler for tiled neural network computations | [![Paper][paper-badge]](https://dl.acm.org/doi/10.1145/3315508.3329973) [![Docs][docs-badge]](https://triton-lang.org/) | [![Code][code-badge]](https://github.com/triton-lang/triton) |
| 2018 Oct | `Apache TVM` | End-to-end optimizing compiler for deep learning | [![Paper][paper-badge]](https://www.usenix.org/conference/osdi18/presentation/chen) [![Docs][docs-badge]](https://tvm.apache.org/) | [![Code][code-badge]](https://github.com/apache/tvm) |
| 2017 Dec | `CUTLASS` | CUDA templates and primitives for high-performance GEMM and related kernels | [![Blog][blog-badge]](https://developer.nvidia.com/blog/cutlass-linear-algebra-cuda/) [![Docs][docs-badge]](https://docs.nvidia.com/cutlass/) | [![Code][code-badge]](https://github.com/NVIDIA/cutlass) |
| - | `MLIR` | Compiler infrastructure for reusable IRs and transformations | [![Docs][docs-badge]](https://mlir.llvm.org/) | [![Code][code-badge]](https://github.com/llvm/llvm-project/tree/main/mlir) |
| - | `IREE` | MLIR-based compiler and runtime for deploying ML workloads across backends | [![Docs][docs-badge]](https://iree.dev/) | [![Code][code-badge]](https://github.com/iree-org/iree) |
| - | `FlashAttention` | IO-aware attention kernels that reshaped the optimization target for LLM systems | [![Paper][paper-badge]](https://arxiv.org/abs/2205.14135) | [![Code][code-badge]](https://github.com/Dao-AILab/flash-attention) |
| - | `ThunderKittens` | Tile-oriented GPU programming primitives for fast custom kernels | - | [![Code][code-badge]](https://github.com/HazyResearch/ThunderKittens) |

[paper-badge]: https://img.shields.io/badge/-Paper-0f766e?style=flat-square
[docs-badge]: https://img.shields.io/badge/-Docs-475569?style=flat-square
[blog-badge]: https://img.shields.io/badge/-Blog-b45309?style=flat-square
[code-badge]: https://img.shields.io/badge/-Code-111827?style=flat-square&logo=github&logoColor=white
