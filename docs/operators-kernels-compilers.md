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

| Date | Venue | Name | Title | Paper / Docs | Code |
|:-:|:-:|:-:|:-|:-:|:-:|
| 2026 May | ArXiv | `FastKernels` | Benchmarking GPU kernel generation in production serving workloads | [![Paper][paper-badge]](https://arxiv.org/abs/2605.23215) | [![Code][code-badge]](https://github.com/Snowflake-AI-Research/fastkernels) |
| 2026 May | ArXiv | `KernelBenchX` | Comprehensive category-aware benchmark for evaluating LLM-generated GPU kernels | [![Paper][paper-badge]](https://arxiv.org/abs/2605.04956) | [![Code][code-badge]](https://github.com/BonnieW05/KernelBenchX) |
| 2025 Jul | ArXiv | `GEAK` | Triton kernel AI agent and evaluation benchmarks for optimized GPU kernels | [![Paper][paper-badge]](https://arxiv.org/abs/2507.23194) | - |
| 2025 Feb | ArXiv | `KernelBench` | Benchmark for testing whether LLMs can write correct and faster GPU kernels | [![Paper][paper-badge]](https://arxiv.org/abs/2502.10517) | [![Code][code-badge]](https://github.com/ZichenZhu/KernelBench_Research) |

### Trained Kernel-Generation Agents

| Date | Venue | Name | Title | Paper / Docs | Code |
|:-:|:-:|:-:|:-|:-:|:-:|
| 2026 Jun | ArXiv | `daVinci-kernel` | Co-evolving skill selection, summarization, and utilization via RL for GPU kernel optimization | [![Paper][paper-badge]](https://arxiv.org/abs/2606.16497) | - |
| 2026 Jun | ArXiv | `MusaCoder` | Native GPU kernel generation with full-stack training on Moore Threads GPU | [![Paper][paper-badge]](https://arxiv.org/abs/2606.04847) | - |
| 2026 Mar | ArXiv | `DRTriton` | Large-scale synthetic data-driven reinforcement learning for Triton kernel generation | [![Paper][paper-badge]](https://arxiv.org/abs/2603.21465) | - |
| 2026 Feb | ArXiv | `Fine-Tuning GPT-5` | Fine-tuning GPT-5 for GPU kernel generation in Makora's training environment | [![Paper][paper-badge]](https://arxiv.org/abs/2602.11000) | - |
| 2026 Feb | ICML 2026 | `Dr. Kernel` | Reinforcement learning done right for Triton kernel generations | [![Paper][paper-badge]](https://arxiv.org/abs/2602.05885) | [![Code][code-badge]](https://github.com/hkust-nlp/KernelGYM) |
| 2025 Oct | ArXiv | `TritonRL` | Training LLMs to think and code Triton without cheating | [![Paper][paper-badge]](https://arxiv.org/abs/2510.17891) | - |
| 2025 Oct | ArXiv | `ConCuR` | Conciseness-oriented training data and KernelCoder for state-of-the-art kernel generation | [![Paper][paper-badge]](https://arxiv.org/abs/2510.07356) | - |
| 2025 Jul | ICLR 2026 | `CUDA-L1` | Improving CUDA optimization via contrastive reinforcement learning | [![Paper][paper-badge]](https://arxiv.org/abs/2507.14111) [![Docs][docs-badge]](https://deepreinforce-ai.github.io/cudal1_blog) | - |

### Agentic Kernel Optimization Frameworks

| Date | Venue | Name | Title | Paper / Docs | Code |
|:-:|:-:|:-:|:-|:-:|:-:|
| 2026 Jun | MLArchSys @ ISCA 2026 | `KForge` | LLM-driven cross-platform kernel generation for AI accelerators | [![Paper][paper-badge]](https://arxiv.org/abs/2606.02963) | - |
| 2026 Mar | ArXiv | `StitchCUDA` | Automated multi-agent end-to-end GPU programming with rubric-based agentic reinforcement learning | [![Paper][paper-badge]](https://arxiv.org/abs/2603.02637) | - |
| 2026 Mar | ArXiv | `KernelFoundry` | Hardware-aware evolutionary GPU kernel optimization with distributed benchmarking | [![Paper][paper-badge]](https://arxiv.org/abs/2603.12440) | - |
| 2026 Mar | ArXiv | `KernelSkill` | Multi-agent GPU kernel optimization with reusable expert skills and trajectory memory | [![Paper][paper-badge]](https://arxiv.org/abs/2603.10085) | [![Code][code-badge]](https://github.com/0satan0/KernelMem) |
| 2026 Jan | ArXiv | `Two-Stage GPU Kernel Tuner` | Semantic refactoring plus search-based optimization for GPU kernel tuning | [![Paper][paper-badge]](https://arxiv.org/abs/2601.12698) | - |
| 2025 Dec | ArXiv | `KernelEvolve` | Scaling agentic kernel coding for heterogeneous AI accelerators at Meta | [![Paper][paper-badge]](https://arxiv.org/abs/2512.23236) | - |
| 2025 Dec | ArXiv | `cuPilot` | Strategy-coordinated multi-agent framework for CUDA kernel evolution | [![Paper][paper-badge]](https://arxiv.org/abs/2512.16465) | [![Code][code-badge]](https://github.com/champloo2878/cuPilot-Kernels) |
| 2025 Nov | ArXiv | `CudaForge` | Agent framework with hardware feedback for CUDA kernel optimization | [![Paper][paper-badge]](https://arxiv.org/abs/2511.01884) | [![Code][code-badge]](https://github.com/OptimAI-Lab/CudaForge) |
| 2025 Oct | ArXiv | `STARK` | Strategic team of agents for refining kernels with profiling feedback | [![Paper][paper-badge]](https://arxiv.org/abs/2510.16996) | - |

### LLM-Agent Algorithm-Discovery Precedents

| Date | Venue | Name | Title | Paper / Docs | Code |
|:-:|:-:|:-:|:-|:-:|:-:|
| 2025 Jun | ArXiv | `AlphaEvolve` | Coding agent for scientific and algorithmic discovery | [![Paper][paper-badge]](https://arxiv.org/abs/2506.13131) | - |
| 2024 Jan | ArXiv | `Evolution of Heuristics` | Automatic algorithm design with large language models | [![Paper][paper-badge]](https://arxiv.org/abs/2401.02051) | [![Code][code-badge]](https://github.com/FeiLiu36/EoH) |
| 2023 Dec | Nature 2023 | `FunSearch` | Mathematical discoveries from program search with large language models | [![Paper][paper-badge]](https://www.nature.com/articles/s41586-023-06924-6) | [![Code][code-badge]](https://github.com/google-deepmind/funsearch) |

## Skills

| Name | What it does | Code |
|:-:|:-|:-:|
| `AKO4ALL` | Drop-in Claude Code skill for iteratively optimizing a supplied GPU kernel with profiling, benchmarking, and rewrite loops. | [![Code][code-badge]](https://github.com/TongmingLAIC/AKO4ALL) |
| `AKO4X` | Closed-loop, campaign-based agent framework for optimizing GPU kernels with swappable benchmarks, per-DSL skills, and optional harness co-evolution. | [![Code][code-badge]](https://github.com/TongmingLAIC/AKO4X) |
| `Kernel Design Agents` | Agent-centric workflow for researching, implementing, verifying, and iterating on performance-sensitive CUDA kernel tasks. | [![Code][code-badge]](https://github.com/mit-han-lab/kernel-design-agents) |
| `ncu-report-skill` | Claude Code skill for building Nsight Compute profiling harnesses, parsing NCU reports, and producing evidence-backed CUDA optimization guidance. | [![Code][code-badge]](https://github.com/mit-han-lab/ncu-report-skill) |
| `KernelWiki` | Claude Code skill and structured knowledge base for Blackwell and Hopper GPU kernel optimization patterns. | [![Code][code-badge]](https://github.com/mit-han-lab/KernelWiki) |
| `AutoKernel` | Autonomous loop that profiles PyTorch models, extracts bottleneck kernels, and optimizes Triton or CUDA C++ replacements with fixed correctness and performance checks. | [![Code][code-badge]](https://github.com/RightNow-AI/autokernel) |
| `AutoMegaKernel` | Agent harness for compiling a model into a verified, self-retargeting CUDA megakernel and self-tuning it for batch-1 LLM decode. | [![Code][code-badge]](https://github.com/RightNow-AI/AutoMegaKernel) |
| `KernelGYM` | Distributed GPU environment for RL training, trajectory collection, and scalable evaluation of kernel generation agents. | [![Code][code-badge]](https://github.com/hkust-nlp/KernelGYM) |
| `CudaForge` | Training-free multi-agent workflow for CUDA kernel generation and optimization using correctness tests and hardware feedback such as Nsight Compute metrics. | [![Code][code-badge]](https://github.com/OptimAI-Lab/CudaForge) |
| `KernelMem` | KernelSkill implementation with memory-aware generation, repair, benchmarking, and NCU/NSYS profiling-driven optimization prompts. | [![Code][code-badge]](https://github.com/0satan0/KernelMem) |

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
