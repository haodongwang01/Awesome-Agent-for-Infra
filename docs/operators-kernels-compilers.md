# Agent for Operators, Kernels and Compilers

[Back to README](../README.md)

## Core Problem

Can agents generate, repair, and optimize the low-level code that determines real model performance?

This track covers CUDA, Triton, tensor programs, compiler schedules, graph rewrites, MLIR/LLVM-style transformations, and profiling-guided optimization. The central challenge is to make agents improve speed without breaking numerical contracts, portability, or maintainability.

## Agent Loop

```text
Reference workload -> kernel / schedule / pass -> compile -> test -> profile -> optimize -> retest
```

## Key Questions

- Can an agent produce kernels that are both correct and faster than framework baselines?
- Can it use profiler traces, compiler errors, occupancy reports, and memory-access patterns as feedback?
- Can generated optimizations transfer across GPUs, CPUs, accelerators, and problem sizes?
- Can agents reason over compiler IRs and schedule spaces rather than only source code?

## Skills

| Skill | What it should do |
| --- | --- |
| `torch-to-triton` | Translate PyTorch reference ops into Triton candidates with correctness tests. |
| `cuda-compile-fix` | Repair CUDA/Triton compile failures with minimal semantic drift. |
| `profile-guided-kernel-tune` | Use Nsight, ncu, torch profiler, or benchmark traces to guide changes. |
| `numerics-guard` | Preserve dtype, tolerance, broadcasting, and edge-case contracts. |
| `compiler-pass-agent` | Propose and validate graph rewrites or IR transformations under tests. |
| `autotuning-budget-manager` | Allocate benchmark trials across candidate kernels, schedules, and hardware targets. |

## Paper

This section is organized by the role each paper plays in the agent-for-kernels stack: benchmarks, trained kernel-generation agents, reusable optimization frameworks, and LLM-agent algorithm-discovery precedents.

### Benchmarks and Evaluation

| Paper | Code / Artifact | Why it matters |
| --- | --- | --- |
| [FastKernels: Benchmarking GPU Kernel Generation in Production](https://arxiv.org/abs/2605.23215) | [Snowflake-AI-Research/fastkernels](https://github.com/Snowflake-AI-Research/fastkernels) | Production-aligned kernel benchmark built from representative Transformer architectures to test whether agent-generated kernels survive real serving-stack integration. |
| [KernelBenchX: A Comprehensive Benchmark for Evaluating LLM-Generated GPU Kernels](https://arxiv.org/abs/2605.04956) | [BonnieW05/KernelBenchX](https://github.com/BonnieW05/KernelBenchX) | Extends kernel-generation evaluation with category-aware task analysis and hardware-behavior breakdowns. |
| [Geak: Introducing Triton Kernel AI Agent & Evaluation Benchmarks](https://arxiv.org/abs/2507.23194) | Not released | Introduces Triton kernel evaluation benchmarks for AMD GPUs alongside an inference-time reasoning loop for generating optimized Triton kernels. |
| [KernelBench: Can LLMs Write Efficient GPU Kernels?](https://arxiv.org/abs/2502.10517) | [ZichenZhu/KernelBench_Research](https://github.com/ZichenZhu/KernelBench_Research) | Benchmark for testing whether LLMs can generate GPU kernels that are both correct and faster than PyTorch references. |

### Trained Kernel-Generation Agents

| Paper | Code / Artifact | Why it matters |
| --- | --- | --- |
| [daVinci-kernel: Co-Evolving Skill Selection, Summarization, and Utilization via RL for GPU Kernel Optimization](https://arxiv.org/abs/2606.16497) | Not released | Jointly trains skill selection, policy, and skill summarization agents so successful CUDA/Triton optimization trajectories become reusable skills. |
| [MusaCoder: Native GPU Kernel Generation with Full-Stack Training on Moore Threads GPU](https://arxiv.org/abs/2606.04847) | Not released | Combines kernel-oriented data synthesis, rejection fine-tuning, and execution-feedback RL for CUDA and MUSA kernel generation. |
| [DRTriton: Large-Scale Synthetic Data Driven Reinforcement Learning for Triton Kernel Generation](https://arxiv.org/abs/2603.21465) | Not released | Trains a PyTorch-to-Triton generator with synthetic operator programs, curriculum RL, decoupled rewards, and test-time search. |
| [Fine-Tuning GPT-5 for GPU Kernel Generation](https://arxiv.org/abs/2602.11000) | Not released | Reports RL fine-tuning of a frontier model for Triton kernel generation in Makora's training environment and evaluates it on KernelBench. |
| [Dr. Kernel: Reinforcement Learning Done Right for Triton Kernel Generations](https://arxiv.org/abs/2602.05885) | [hkust-nlp/KernelGYM](https://github.com/hkust-nlp/KernelGYM) | Releases KernelGYM and studies multi-turn RL methods, profiling-based rewards, and reward-hacking checks for Triton kernel generation. |
| [TritonRL: Training LLMs to Think and Code Triton Without Cheating](https://arxiv.org/abs/2510.17891) | Not released | Trains an 8B Triton-specialized model with SFT plus RL, using layered verification to prevent reward hacking while optimizing correctness and speed. |
| [ConCuR: Conciseness Makes State-of-the-Art Kernel Generation](https://arxiv.org/abs/2510.07356) | Not released | Builds ConCuR data and KernelCoder from curated PyTorch, reasoning, and CUDA kernel pairs, emphasizing concise reasoning traces. |
| [CUDA-L1: Improving CUDA Optimization via Contrastive Reinforcement Learning](https://arxiv.org/abs/2507.14111) | [Project](https://deepreinforce-ai.github.io/cudal1_blog) | Uses contrastive RL to train an LLM for CUDA optimization with speedup-based rewards, portability checks, and reward-hacking safeguards. |

### Agentic Kernel Optimization Frameworks

| Paper | Code / Artifact | Why it matters |
| --- | --- | --- |
| [KForge: LLM-Driven Cross-Platform Kernel Generation for AI Accelerators](https://arxiv.org/abs/2606.02963) | Not released | Uses collaborating generation and performance-analysis agents to iteratively produce kernels across heterogeneous accelerator backends. |
| [StitchCUDA: An Automated Multi-Agents End-to-End GPU Programing Framework with Rubric-based Agentic Reinforcement Learning](https://arxiv.org/abs/2603.02637) | Not released | Extends kernel optimization toward end-to-end GPU programs with planner, coder, and verifier agents plus execution-based rubric rewards. |
| [KernelSkill: A Multi-Agent Framework for GPU Kernel Optimization](https://arxiv.org/abs/2603.10085) | [0satan0/KernelMem](https://github.com/0satan0/KernelMem/) | Multi-agent kernel optimization framework built around reusable expert skills and trajectory memory. |
| [KernelFoundry: Hardware-aware Evolutionary GPU Kernel Optimization](https://arxiv.org/abs/2603.12440) | Not released | Hardware-aware evolutionary kernel optimization framework with distributed benchmarking and candidate selection. |
| [A Two-Stage GPU Kernel Tuner Combining Semantic Refactoring and Search-Based Optimization](https://arxiv.org/abs/2601.12698) | Not released | Combines an agent-driven semantic refactoring loop with constrained search over explicit kernel-template parameters. |
| [KernelEvolve: Scaling Agentic Kernel Coding for Heterogeneous AI Accelerators at Meta](https://arxiv.org/abs/2512.23236) | Not released | Production-scale agentic kernel coding framework that searches across Triton, CuTe DSL, and lower-level abstractions for heterogeneous accelerators. |
| [cuPilot: A Strategy-Coordinated Multi-agent Framework for CUDA Kernel Evolution](https://arxiv.org/abs/2512.16465) | [champloo2878/cuPilot-Kernels](https://github.com/champloo2878/cuPilot-Kernels) | Evolves CUDA kernels through strategy-level representations, roofline-guided prompting, and coordinated multi-agent search. |
| [CudaForge: An Agent Framework with Hardware Feedback for CUDA Kernel Optimization](https://arxiv.org/abs/2511.01884) | [OptimAI-Lab/CudaForge](https://github.com/OptimAI-Lab/CudaForge) | Training-free multi-agent CUDA optimizer that uses correctness tests and hardware feedback such as Nsight Compute metrics. |
| [STARK: Strategic Team of Agents for Refining Kernels](https://arxiv.org/abs/2510.16996) | Not released | Multi-agent kernel refinement framework with grounded instructions, dynamic context management, strategic search, and profiling feedback. |

### LLM-Agent Algorithm-Discovery Precedents

| Paper | Code / Artifact | Why it matters |
| --- | --- | --- |
| [AlphaEvolve: A Coding Agent for Scientific and Algorithmic Discovery](https://arxiv.org/abs/2506.13131) | Not released | General-purpose evolutionary coding agent that uses LLM-generated code edits plus executable evaluators to discover algorithms and optimize infrastructure components. |
| [Evolution of Heuristics: Towards Efficient Automatic Algorithm Design Using Large Language Model](https://arxiv.org/abs/2401.02051) | [FeiLiu36/EoH](https://github.com/FeiLiu36/EoH) | Evolves natural-language heuristic ideas and executable code with LLMs, establishing a practical open framework for automatic heuristic design. |
| [FunSearch: Mathematical Discoveries from Program Search with Large Language Models](https://www.nature.com/articles/s41586-023-06924-6) | [google-deepmind/funsearch](https://github.com/google-deepmind/funsearch) | Combines LLM-generated programs with an evaluator and evolutionary selection to discover new mathematical constructions and optimization heuristics. |

## Toolchain

| Toolchain | Role in the agent loop |
| --- | --- |
| [Apache TVM](https://github.com/apache/tvm) | Tensor compiler stack with auto-scheduling and hardware-aware optimization workflows. |
| [Triton](https://github.com/triton-lang/triton) | Python-like DSL and compiler for writing efficient GPU kernels. |
| [MLIR](https://mlir.llvm.org/) | Compiler infrastructure for reusable IRs and transformations. |
| [IREE](https://github.com/iree-org/iree) | MLIR-based compiler and runtime for deploying ML workloads across backends. |
| [CUTLASS](https://github.com/NVIDIA/cutlass) | CUDA templates and primitives for high-performance GEMM and related kernels. |
| [FlashAttention](https://github.com/Dao-AILab/flash-attention) | IO-aware attention kernels that reshaped the optimization target for LLM systems. |
| [ThunderKittens](https://github.com/HazyResearch/ThunderKittens) | Tile-oriented GPU programming primitives for fast custom kernels. |

## Evaluation Signals

| Signal | Examples |
| --- | --- |
| Correctness | Numerical tolerance, dtype coverage, shape coverage, edge cases |
| Performance | Runtime, bandwidth, FLOP utilization, occupancy, speedup over baseline |
| Compilation | Compile success, compile time, generated code quality, portability |
| Robustness | Problem-size shifts, GPU architecture shifts, driver/compiler version shifts |
| Cost | Tuning budget, benchmark time, hardware hours |
