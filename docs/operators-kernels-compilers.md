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

| Paper | Why it matters |
| --- | --- |
| [KernelBench](https://arxiv.org/abs/2502.10517) | Evaluates whether LLMs can write correct and faster GPU kernels for PyTorch workloads. |
| [KernelBench-X](https://arxiv.org/abs/2605.04956) | Category-aware benchmark for LLM-generated GPU kernels across task types and hardware behavior. |
| [KernelSkill](https://arxiv.org/abs/2603.10085) | Multi-agent kernel optimization framework built around reusable expert skills and trajectory memory. |
| [KernelFoundry](https://arxiv.org/abs/2603.12440) | Hardware-aware evolutionary kernel optimization with distributed benchmarking. |
| [AlphaTensor](https://www.nature.com/articles/s41586-022-05172-4) | Reinforcement learning for discovering matrix multiplication algorithms. |
| [AlphaDev](https://www.nature.com/articles/s41586-023-06004-9) | AI-discovered sorting algorithms, a useful precedent for agentic low-level optimization. |
| [Ansor](https://arxiv.org/abs/2006.06762) | Search-based auto-scheduler for tensor programs. |

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
